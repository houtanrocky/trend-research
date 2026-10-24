# T1 Research Plan — Invariant-Preserving Coding Agents on Stateful Backends

Status: draft for execution. This document is the working plan for the recommended primary track.

## 1. Working title

**"Do Coding Agents Preserve Transactional Invariants? A Pilot Benchmark on Stateful Backend Systems."**

## 2. Problem statement

Existing code-generation benchmarks (SWE-bench and successors) score agents by whether unit tests pass after an edit. That criterion is insufficient for stateful systems: an agent can make tests pass while introducing double-spending, lost updates, phantom reservations, or non-idempotent retries. In financial and marketplace backends, these are exactly the failures that matter and exactly the failures that tests rarely cover.

**Gap:** there is no accepted benchmark that measures *transactional invariant preservation* under agent-generated edits, and no evidence on whether invariant-oriented guidance improves outcomes.

## 3. Research questions

- **RQ1 (descriptive):** When coding agents implement feature requests on a stateful backend, how often do they violate pre-existing transactional invariants?
- **RQ2 (interventional):** Does invariant-oriented guidance (explicit invariant specification plus required state checks in the prompt) reduce the violation rate relative to a standard feature-request prompt?
- **RQ3 (cost):** What is the effect on task completion, latency, and token cost?
- **RQ4 (qualitative):** What failure modes recur across agents and tasks?

## 4. Hypotheses

- **H1 (null, RQ1 baseline):** Agents produce invariant violations in a non-trivial fraction of runs (expected > 20%). If the observed rate is near zero, the benchmark is too easy and must be hardened before drawing conclusions.
- **H2:** Invariant-oriented guidance reduces the violation rate relative to the control condition.
- **H3:** Invariant-oriented guidance does not reduce task completion below a pre-specified threshold (e.g. no more than 10 percentage points).
- **H4:** Failure modes cluster into a small taxonomy (see section 8), which is a finding in its own right.

## 5. Target system

**Dragon Market** (`houtanrocky/dragon-market`), pinned at commit `f4ba21185d1ba7b4bbb56f5addcc27d1b75bdec7`.

Why this target:
- Real transactional semantics: wallet balances, wallet reservations, timed auctions, fixed-price orders, idempotent payments.
- Go plus PostgreSQL plus Docker Compose plus Testcontainers: deterministic, containerised, reproducible.
- Already has an independent state-check pattern and a documented historical failure baseline (`162c5ca`).
- Small enough to run 36 executions in a reasonable time window.

Risk: only one target system means limited external validity. Mitigation: explicitly frame the study as a **pilot** and a **benchmark contribution**, not a general claim about all backends.

## 6. Task packages

Each package must contain: (a) a natural-language feature request, (b) a reference solution, (c) independent state checks separate from feature tests, (d) at least one rejected faulty variant used to validate that the checks actually detect violations, and (e) a declared invariant list.

| ID | Task | Core invariants under test |
|---|---|---|
| T001 | Purchase retries (idempotent payment under retry) | No double debit; exactly one order; retry returns the same result |
| T002 | Auction close race (concurrent bids at deadline) | Single winner; no bid accepted after close; wallet reservation released or consumed exactly once |
| T003 | Wallet reservation expiry (hold then expire) | Reservation cannot be double-spent; expiry releases funds exactly once; no negative balance |

Package acceptance gate: the faulty variant **must** fail the state checks while the reference solution **must** pass them. If a faulty variant passes, the checks are inadequate and the package is not approved.

**Current status:** T001 exists in draft. T002 and T003 must be authored. Independent human baseline approval is outstanding and is a blocking gate.

## 7. Experimental design (pilot scale)

| Factor | Levels |
|---|---|
| Task | T001, T002, T003 (3) |
| Agent system | 2 systems (one primary, one secondary; recorded by name and version) |
| Condition | Control (standard feature request) vs. Treatment (invariant-oriented guidance) |
| Repetition | 3 runs per cell |

**Total:** 3 x 2 x 2 x 3 = **36 runs.**

The 96-run ceiling in the existing design is retained only as a declared upper bound; it is **not** the target. Rationale: 36 runs is the largest design that remains feasible solo, within budget, and analysable with honest uncertainty.

**Randomisation:** run order must be randomised and recorded, to avoid confounding by time-of-day API behaviour or model updates.

**Contamination control:** record model name and version and the API snapshot date for every run. If the provider changes the model mid-study, split the analysis and report it.

## 8. Metrics

**Primary outcome**
- **Invariant violation rate:** fraction of runs in which at least one independent state check fails.

**Secondary outcomes**
- Feature-test pass rate (did the requested behaviour work?).
- Number of distinct invariant violations per run.
- Latency per run and token cost per run.
- Human review time per run (optional, if a reviewer is available).

**Violation taxonomy** (used for classification and for the qualitative analysis):
1. Double-spend (funds debited twice).
2. Lost update (concurrent write overwrites another).
3. Phantom reservation (reserved funds are neither spent nor released).
4. Non-idempotent retry (repeated request produces a second effect).
5. Rollback inconsistency (partial state persists after failure).
6. Post-close acceptance (bid or order accepted outside its valid window).

## 9. Analysis plan (pre-registered before running)

- Report the violation rate per cell with exact counts, plus Wilson 95% intervals. With n=9 per cell, intervals will be wide; this must be stated plainly.
- Primary comparison: treatment versus control, pooled across tasks and systems, reported as a difference in proportions with an interval. Do **not** report a p-value as if the study were powered; report it, if at all, as descriptive.
- Secondary: per-task and per-system breakdowns, presented as exploratory.
- Report cost and latency descriptively (median, IQR).
- Publish all raw run records, traces, diffs, and SHA-256 manifests.

**Explicit non-claims:** no causal claim about all agents, all backends, or all task types. This is a pilot on one system.

## 10. Threats to validity

| Threat | Mitigation |
|---|---|
| Single target system | Frame as pilot; invite replication; publish harness so others can add targets. |
| Small n | Report intervals honestly; avoid inferential overreach. |
| Model version drift | Record version and date per run; split analysis if the model changes. |
| Task author bias | Independent reviewer approves baselines and state checks. |
| Test leakage in prompts | Prompt must not contain the state checks themselves in the control condition. |
| Agent gaming (editing tests) | State checks live outside the agent's editable tree and are re-applied after each run. |
| Reproducibility | Pin target commit, harness version, container images, and random seed where applicable. |

## 11. Timeline (24 weeks)

| Weeks | Milestone |
|---|---|
| 1-2 | Freeze scope at 36 runs. Publish pre-registration (hypotheses, metrics, analysis plan). |
| 3-6 | Harden T001; author T002 and T003 with rejected faulty variants. Obtain independent baseline approval. |
| 5-8 | Finalise harness instrumentation: traces, diffs, manifests, violation classifier. Freeze harness version. |
| 9-12 | Execute 36 runs in randomised order. Monitor cost. |
| 13-16 | Analysis; qualitative failure-mode coding; draft report. |
| 17-20 | Preprint and public harness release; workshop submission. |
| 21-24 | Blog series, talk, and scoping of the T3 guardrail product prototype. |

## 12. Deliverables and acceptance criteria

The track is **done** when all five exist:

1. **Public pre-registration** document, timestamped before any run.
2. **Three approved task packages**, each with a reference solution, independent state checks, and at least one rejected faulty variant that the checks correctly catch.
3. **Public harness release** with pinned versions and reproducible instructions.
4. **Reproducible pilot report** with 36 runs, raw records, and honest intervals.
5. **Preprint** (arXiv or workshop) with the taxonomy and the descriptive findings.

A null result on H2 still satisfies the acceptance criteria, provided the benchmark and report are published. That is a deliberate design choice: the artifact must be valuable independently of the headline result.

## 13. Budget estimate

- 36 runs x 2 conditions are already counted in the 36; each run may consume multiple agent turns.
- Assume 20-60 agent turns per run at current frontier-model pricing. Estimate the total at low hundreds of USD, not thousands.
- Infrastructure: local Docker plus PostgreSQL; no paid database needed.
- Contingency: budget 2x the initial estimate for retries and re-runs after harness bugs.

## 14. What would make this fail

1. **Baseline too easy.** If the control condition produces near-zero violations, the benchmark is not discriminating. Response: harden tasks until a known faulty variant is caught and a naive-but-plausible implementation is caught.
2. **Baseline too hard.** If both conditions produce near-100% violations, there is no signal. Response: add hints to the feature request, not to the invariant specification.
3. **Agent edits the checks.** Response: checks live outside the editable tree and are re-applied.
4. **Scope creep to 96 runs.** Response: the pre-registration says 36; anything more is a follow-up study.
5. **No independent reviewer.** Response: the credibility gate is mandatory; without it, publish as a "provisional pilot" with the limitation stated in the title or abstract.

## 15. Relationship to other tracks

- **T10 (harness as open standard):** this plan's artifact is T10. Ship the harness with the paper.
- **T8 (verification):** the violation taxonomy and state-check machinery is T8. It is the instrument, not a separate study.
- **T3 (guardrails):** the findings feed a guardrail product. Do not start the product before the pilot report.
- **T2 (metro-premium):** unrelated; keep as a parallel hedge at low intensity.