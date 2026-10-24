# Trend Research — Research Topic Evaluation for Houtan Rocky

**Prepared:** 2026-10-24
**Subject:** Houtan Abasi Rocky ([houtanrocky.com](https://houtanrocky.com), [github.com/houtanrocky](https://github.com/houtanrocky))
**Question:** Which research topics are the best fit and highest-value direction for this researcher?

---

## TL;DR — The Recommendation

**Primary track: "Invariant-Preserving Coding Agents" (AI-assisted software engineering on stateful backends).**

You have already started exactly the right thing — `agent-invariant-preservation` — and it sits at the intersection of your three rarest, hardest-to-copy assets:

1. **Deep, hands-on concurrency/transaction engineering** (Dragon Market: Go + PostgreSQL + wallets + auctions + idempotency + Testcontainers).
2. **A finished, credible empirical-research methodology** (metro-premium: source audits, explicit uncertainty gates, reproducible pipelines, bilingual publication).
3. **A real MSc-level research framing** (theory, experimental design, falsifiable hypothesis, pre-registered metrics).

Almost nobody in the AI-coding-agent literature has your combination of *production-grade transactional systems* and *research discipline*. That is your unfair advantage. **Commit to it.**

**Secondary track (portfolio hedge): "Computational Urban Economics / Geo-Spatial Data Science for Iran."** Keep `metro-premium` alive — it is publishable, distinctive, and locally defensible. But do not let it become the main track; it competes in a crowded global field and lacks the compounding professional leverage of track 1.

**Do not pursue:** generic LLM app-building, generic Web3/dApp research, Chrome-extension tooling research, or framework/tutorial repos. These have no research ceiling and no differentiated audience.

---

## 1. Profile Analysis (evidence-based)

### 1.1 Who you are, from your own materials

| Signal | Evidence | What it tells us |
|---|---|---|
| 8+ years shipping systems | Site "At a glance": 8+ years, 11 selected projects, 5 tools shipped | Operator-engineer, not a first-time researcher. You can build real systems. |
| Fintech at organizational scale | **Nafisagold** — gold-credit platform for Bime Salamat, **4,400 personnel**, async credit engine, e-sign, Pasargad PSP; Technical Team Lead; NestJS / React / RabbitMQ / Redis / PostgreSQL | You have shipped *money-moving, stateful, auditable* systems under real constraints. Single most valuable domain asset. |
| Backend systems depth | **Dragon Market** — Go, PostgreSQL transactions, auctions, wallet reservations, idempotent payments, Docker, Testcontainers, 17 GitHub topics | You know exactly where the bugs are: races, double-selling, idempotency, rollback semantics. |
| Web3 / real-time | **Hidden Bitcoin/Crypto Hunt** — React-Vite, Go, gRPC-Web, Three.js, Subsquid/TheGraph; **uniswap-widget** (3 stars); **TON-Testnet-Transaction-App** | Real Web3 work, but as a *developer*, not a protocol researcher. |
| AI product work | **Breeze.ai** (AI gaming image editing, React/Firebase); **Commerceflow.ai** (image to marketing text) | You integrated AI as a product feature. Strong on AI *engineering*, thin on AI *science*. |
| AI research (nascent) | **agent-invariant-preservation** — "Preserving Transactional Invariants in AI-Assisted Software Development"; MSc foundation; 8x2x2x3 = 96-run ceiling; Dragon Market as subject; operational pin f4ba211… | **A real research program already in motion**, with proposal, design, reading list, benchmark packages, target baseline. |
| Research discipline | **metro-premium** — 1,000,000-row source audit, 84,586 Tehran listings filtered to 3,110 candidates, 555,686-node OSM graph, 166 entrances / 2,978 routes, explicit "no operational premium established", bilingual EN/FA publication | You already know how to run a *defensible* empirical study and refuse to overclaim. Rare, and exactly what agent-evaluation lacks. |
| Open-source reach | 93 public repos (68 originals, 25 forks), 8 gists, 90 followers. Top: Terminal Copy On Select (5 stars), Iranian Banks React Icons (4), Uniswap Widget (3) | Your OSS is *tooling*: useful, but small-scale. Research repos compound better. |
| Breadth, not focus | Go, TypeScript, Python, JS, Svelte, Vue, PHP, Lua, SCSS, Jupyter; ~20 domains | Strength as a builder, weakness as a researcher. Research rewards narrow depth. |
| Stated identity | Bio: "Development / Design / Strategy — Sweat and grit, not wishful thinking"; site: "Independent engineer for ambitious products"; Tehran, Iran | You want to be an independent authority, not a cog. Research is the vehicle. |

### 1.2 The strategic read

You are at a **rare inflection point**: senior-level systems credentials, a functioning research apparatus, and *two* live research repos. The bottleneck is not capability — it is **commitment and focus**. Your history shows parallel bets (Web3 widget, games, a taxi app, Chrome extensions, a geo study, an agent study) with no single line compounding for more than a few weeks.

**Research only pays if it compounds.** One finished, cited, well-defended study beats ten started repos. The evaluation below ranks on *compounding leverage*, not novelty alone.

---

## 2. Evaluation Framework

Each candidate topic is scored 1-5 on seven criteria; weighted total = sum(score x weight).

| Criterion | Weight | Why it matters |
|---|---:|---|
| Fit with proven skills | 20% | Can you execute without a six-month detour into a new field? |
| Unfair advantage / moat | 20% | Could a typical researcher do this at all, let alone as well? |
| Research ceiling | 15% | Can it yield a paper, thesis, benchmark, or artifact others cite? |
| Practical leverage | 15% | Does it convert into jobs, consulting, speaking, or products? |
| Feasibility in 4-6 months | 15% | Solo, self-funded, no lab? |
| Novelty / white space | 10% | Is it underexplored *right now*? |
| Personal momentum | 5% | Have you already started and stayed interested? |

---

## 3. Candidate Topics — Scored

### T1. Invariant-Preserving Coding Agents on Stateful Backends — RECOMMENDED PRIMARY

> *How reliably can LLM coding agents modify transactional backend systems without breaking invariants (no double-spend, no lost update, idempotency preserved, rollback correct)? Does invariant-oriented prompting or verification improve correctness?*

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 5 | You built Dragon Market exactly for this. |
| Moat | 5 | Few AI-SE researchers can build a concurrency-correct Go/Postgres target plus a real benchmark harness. |
| Research ceiling | 5 | Benchmarks get cited; "invariant preservation" is a named, unsolved problem. |
| Practical leverage | 5 | Directly sellable: AI code review, agent guardrails, enterprise AI adoption. |
| Feasibility | 4 | 96-run ceiling is heavy; must be cut to a pilot. |
| Novelty | 5 | Agent evaluation on *stateful* systems is nascent; most benchmarks are stateless, SWE-bench-like. |
| Momentum | 5 | Repo, design, packages and pin already exist. |
| **Weighted** | **4.90** | Clear winner. |

**Concrete framing:** *"SWE-bench measures whether tests pass. It does not measure whether money is conserved."* Your contribution is a benchmark plus protocol for **transactional invariant preservation** under agent edits, with injectable faulty variants and human-approved baselines.

**Risks:** (a) LLM API cost and variance for 2 systems x 2 conditions; (b) reviewer skepticism of small n; (c) scope creep.
**Mitigations:** pilot at 2 tasks x 2 systems x 1 condition x 3 reps = 12 runs; pre-register; publish the harness as an open artifact even if results are null.

---

### T2. Geo-Spatial Housing and Accessibility Analysis (metro-premium line) — SECONDARY

> *Network-based analysis of Tehran asking prices vs. metro walking access, with explicit uncertainty and privacy gates.*

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 4 | Python pipeline plus React publication — already proven. |
| Moat | 3 | Urban economists do this routinely; your moat is local data access and honest uncertainty handling, not method. |
| Research ceiling | 4 | Publishable in applied geo/urban venues; bilingual EN/FA is a differentiator. |
| Practical leverage | 3 | Consulting for Iranian real estate or policy; limited global hiring signal. |
| Feasibility | 4 | Pipeline exists; remaining work is topology and entrance validation. |
| Novelty | 3 | Metro-premium studies are well trodden globally; Iran-specific is thinner but small. |
| Momentum | 4 | Active and well documented. |
| **Weighted** | **3.55** | Strong hedge, not the main bet. |

**Concrete framing:** finish the *defensible descriptive* paper ("what can and cannot be claimed from public listing data"), then stop. Do not chase causal identification.

---

### T3. AI Agent Guardrails and Runtime Policy Enforcement for Money Movement

> *Can a runtime policy layer (Kill Switch generalized) provably constrain what an autonomous agent may do to a financial system?*

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 4 | Kill Switch, fintech, agent work. |
| Moat | 4 | Very few people build *enforcement* rather than *evaluation*. |
| Research ceiling | 3 | Strong engineering paper or artifact; less of a scientific result. |
| Practical leverage | 5 | Highest commercial value of all topics; agent safety for fintech is a live budget line. |
| Feasibility | 4 | Prototype in weeks. |
| Novelty | 4 | Agent safety is hot; *enforcement on transactional APIs* is thinner. |
| Momentum | 3 | Adjacent, not started. |
| **Weighted** | **3.90** | Excellent *product* bet; weaker as first *research* bet. Spin-off from T1. |

---

### T4. LLM-Based Evaluation of Open-Source Repository Quality and Maintainability

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 4 | You have built and reviewed many repos. |
| Moat | 2 | Extremely crowded (CodeRabbit, Snyk, Sonar, academic metric papers). |
| Research ceiling | 3 | Metric-validation papers are publishable but low prestige. |
| Practical leverage | 4 | SaaS-able. |
| Feasibility | 4 | Doable. |
| Novelty | 2 | Saturated. |
| Momentum | 1 | Not started. |
| **Weighted** | **3.00** | Commodity; you would be one of a thousand. Skip. |

---

### T5. Web3 Protocol and DeFi Mechanism Research

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 3 | A Uniswap widget is integration, not mechanism design. |
| Moat | 2 | Protocol researchers are deep specialists (game theory, cryptography). |
| Research ceiling | 4 | High prestige, but requires math/crypto foundations you would have to build. |
| Practical leverage | 2 | Volatile market; sanctions friction for global roles. |
| Feasibility | 2 | High barrier; data access and capital for experiments. |
| Novelty | 3 | Crowded. |
| Momentum | 1 | Dormant. |
| **Weighted** | **2.55** | Wrong battlefield. |

---

### T6. Developer Tooling and Browser-Extension UX Research

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 5 | You ship these. |
| Moat | 2 | Trivial to replicate. |
| Research ceiling | 2 | Not a research field; at best a blog post or n=10 HCI workshop. |
| Practical leverage | 2 | Low. |
| Feasibility | 5 | Easy. |
| Novelty | 1 | None. |
| Momentum | 3 | Several live repos. |
| **Weighted** | **2.70** | Build them as *products*, not as *research*. |

---

### T7. LLM-Assisted Education and Localized Learning Tools (Persian)

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 4 | Udemy helper repos; teaching instinct. |
| Moat | 3 | Persian-language market is underserved. |
| Research ceiling | 3 | LAK/AIED venues exist but require education theory. |
| Practical leverage | 4 | Real market in Iran; monetizable. |
| Feasibility | 4 | Feasible. |
| Novelty | 3 | Moderate. |
| Momentum | 2 | Adjacent repos only. |
| **Weighted** | **3.45** | Good *business*, mediocre *research*. Product line, not thesis. |

---

### T8. Reliability Engineering for AI-Generated Code (Static and Semantic Verification)

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 4 | Dragon Market's Testcontainers and transaction tests are exactly this. |
| Moat | 4 | Combines concurrency with verification. |
| Research ceiling | 4 | Verifiable standalone or as part of T1. |
| Practical leverage | 5 | CI vendors would pay. |
| Feasibility | 4 | Buildable incrementally. |
| Novelty | 4 | "Agent plus property-based testing on DB transactions" is thin. |
| Momentum | 3 | Implied by the T1 harness. |
| **Weighted** | **3.95** | **Best sub-topic to fold into T1** — it is the *mechanism* T1 evaluates. |

---

### T9. Distributed Systems Pedagogy and Reference Architectures (Dragon-Market-as-textbook)

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 5 | Already the artifact. |
| Moat | 4 | Explanations plus working code is a rare pairing. |
| Research ceiling | 2 | Not research; education and advocacy. |
| Practical leverage | 4 | Reputation, talks, courses, hiring. |
| Feasibility | 5 | Nearly done. |
| Novelty | 2 | Many such references exist, fewer with Testcontainers plus idempotency focus. |
| Momentum | 4 | Active. |
| **Weighted** | **3.60** | High-ROI *supporting* activity, not a research track. |

---

### T10. AI Coding Agent Benchmark Infrastructure (harness/runner as an open standard)

| Criterion | Score | Rationale |
|---|---:|---|
| Skill fit | 5 | Already partly built. |
| Moat | 4 | Early mover. |
| Research ceiling | 3 | Infrastructure papers get cited; not the headline result. |
| Practical leverage | 5 | Standards equal authority. |
| Feasibility | 4 | Incremental. |
| Novelty | 4 | Very few stateful-agent harnesses. |
| Momentum | 5 | Exists. |
| **Weighted** | **4.35** | **Fold into T1 as its artifact contribution.** |

---

## 4. Ranking Summary

| Rank | Topic | Weighted | Verdict |
|---:|---|---:|---|
| 1 | **T1 Invariant-Preserving Coding Agents** | **4.90** | **Primary track — commit.** |
| 2 | T10 Benchmark harness as artifact | 4.35 | Fold into T1. |
| 3 | T8 Verification and property tests for agent code | 3.95 | Fold into T1. |
| 4 | T3 Agent guardrails for money movement | 3.90 | Spin-off / product. |
| 5 | T9 Dragon Market as reference architecture | 3.60 | Supporting activity. |
| 6 | T2 Metro and housing geo research | 3.55 | Secondary hedge. |
| 7 | T7 Persian LLM education tools | 3.45 | Product idea, not thesis. |
| 8 | T4 LLM repo-quality evaluation | 3.00 | Skip. |
| 9 | T6 Dev tooling UX research | 2.70 | Build as product only. |
| 10 | T5 Web3 mechanism research | 2.55 | Skip. |

Full matrix and sensitivity analysis: `docs/topic-scorecard.md`.

---

## 5. Why T1 Is the Right Bet (the argument in one page)

1. **You are one of very few people who can build the target system correctly.** Most agent-evaluation papers use toy repos or stateless tasks. Dragon Market has real transactional invariants: wallet balances, auction close, idempotent payment, reservation expiry. Building a *fault-injectable* version of that is itself a contribution.
2. **The research question is crisp and falsifiable.** H0: invariant-oriented guidance does not change the rate of invariant violations. H1: it reduces violations without reducing task completion. Both are measurable.
3. **The artifact outlives the result.** Even a null result yields a benchmark and harness the community can use — with your name on it.
4. **It converts directly into money.** "I build guardrails and evaluations for AI agents touching financial systems" is a premium consulting and hiring position in 2026-2027.
5. **It compounds with everything else you have.** Fintech (Nafisagold), Go/Postgres (Dragon Market), research method (metro-premium), agent tooling (Kill Switch, researchctl) — all four feed T1. No other topic uses all four.
6. **It is defensible against bigger labs.** Labs have GPUs and model access; they do not have your production-transaction intuition or your willingness to build careful, boring, correct benchmarks.

**The one-line identity to own:**
> *"I study whether AI coding agents can be trusted with money."*

---

## 6. Recommended 6-Month Plan (T1)

**Phase 0 — Scope cut (weeks 1-2)**
- Freeze the design at **pilot scale**: 3 tasks x 2 agent systems x 2 conditions x 3 reps = 36 runs. Declare the 96-run design the *ceiling*, not the target.
- Publish a pre-registration document (hypothesis, metrics, exclusion rules, analysis plan) before running anything.

**Phase 1 — Benchmark hardening (weeks 3-6)**
- Finalize T001 (purchase retries); add T002 (auction close race) and T003 (wallet reservation expiry).
- Each package: reference solution, independent state checks, at least one **rejected faulty variant** (already your pattern).
- Human baseline approval: get one independent reviewer to sign the baseline. This is the credibility gate.

**Phase 2 — Harness and metrics (weeks 5-8)**
- Define an invariant violation taxonomy: double-spend, lost update, phantom reservation, non-idempotent retry, rollback inconsistency.
- Instrument `researchctl` to record traces, diffs, and per-run manifests (SHA-256), as it already does.
- Freeze harness version and pin the target commit.

**Phase 3 — Pilot runs (weeks 9-12)**
- Run 36 executions. Record cost, latency, and variance.
- Report violation rate per condition, task completion, and qualitative failure modes.

**Phase 4 — Write-up (weeks 13-20)**
- Technical report or arXiv preprint: *"Do Coding Agents Preserve Transactional Invariants? A Pilot Benchmark."*
- Open-source the harness and benchmark packages.
- One workshop or conference submission (AI-SE workshop, ICSE/FSE workshop track, or NeurIPS Datasets and Benchmarks if scope justifies it).

**Phase 5 — Leverage (weeks 20-24)**
- Blog series on houtanrocky.com.
- Talk or podcast.
- Turn T3 (guardrails) into a product prototype using the findings.

**Acceptance criteria for "done":** a public preprint, a public harness, three approved task packages, and a reproducible pilot report. Nothing less counts.

---

## 7. Guardrails (what to stop doing)

- **Stop starting new repos** until T1 has a preprint. Your repo count is already a distraction signal.
- **Do not expand metro-premium** beyond one descriptive paper.
- **Do not chase Web3 research**; keep the widget as a portfolio piece.
- **Do not turn T1 into a product** before the pilot report exists — evaluation first, guardrail product second.
- **Cap context-switching**: one primary track, one hedge, tools only as needed.

---

## 8. Files in this repo

| File | Contents |
|---|---|
| `README.md` | This evaluation (primary deliverable) |
| `docs/profile-analysis.md` | Extended evidence table and source notes |
| `docs/topic-scorecard.md` | Full scoring matrix and sensitivity analysis |
| `docs/t1-research-plan.md` | Detailed T1 plan: hypotheses, metrics, risks |
| `docs/alternatives.md` | Deeper notes on T2-T10 |
| `docs/tmu-research.md` | Tarbiat Modares University (ISE) institutional fit note — evidence, faculty map, verdict |
| `data/ise/` | Raw scraped TMU ISE pages (departments, research areas, faculty) backing the note |
| `data/profile-snapshot.json` | Raw GitHub profile snapshot used |
| `data/repos-snapshot.tsv` | Repo inventory (name, language, stars, pushed, description) |

---

*Prepared as an independent evaluation. All claims about the subject derive from public sources: houtanrocky.com and the public GitHub API for `houtanrocky`. No private information was used.*