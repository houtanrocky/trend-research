# Trend Research — How to Find the Best Research Trend (and the Answer for Houtan Rocky)

**Prepared:** 2026-10-24
**Subject:** Houtan Abasi Rocky ([houtanrocky.com](https://houtanrocky.com), [github.com/houtanrocky](https://github.com/houtanrocky))
**Question:** Which research trend is the best fit and highest-value direction, and how do we decide?

---

## 0. TL;DR — the answer in six lines

1. **Method first.** A "best trend" is not the hottest topic — it is the trend where *fit × moat × compounding leverage* is highest. Section 1 gives the repeatable method.
2. **Winner:** **T1 — Invariant-Preserving Coding Agents on Stateful Backends** (weighted **4.90 / 5**, first under every re-weighting tested).
3. **Hedge:** **T2 — Tehran housing × metro accessibility** (3.55). One descriptive paper, then stop.
4. **Absorb, don't split:** T10 (harness) and T8 (verification) are artifacts *inside* T1; T3 (guardrails) is a later product spin-off.
5. **Institutional anchor:** TMU ISE = strong for T2 (composite 4.5), secondary methodological co-supervision for T1 (3.2).
6. **The one-line identity:** *"I study whether AI coding agents can be trusted with money."*

---

## 1. Method — how to find the best trend (reusable)

Use this whenever a new candidate trend appears. It is deliberately boring; the boring-ness is what stops trend-chasing.

### 1.1 Inventory the assets you already have
List what is **already built or half-built**, with evidence (repos, commits, datasets, shipped products). Trends that *reuse* these assets beat trends that require new ones. Assets for this profile are in `docs/profile-analysis.md`.

### 1.2 Score every candidate on seven criteria
| Criterion | Weight | The question it answers |
|---|---:|---|
| Fit with proven skills | 20% | Can I execute without a six-month detour? |
| Unfair advantage / moat | 20% | Could a typical researcher do this at all, let alone as well? |
| Research ceiling | 15% | Can it yield a paper, thesis, benchmark, or artifact others cite? |
| Practical leverage | 15% | Does it convert into jobs, consulting, speaking, products? |
| Feasibility in 4-6 months | 15% | Solo, self-funded, no lab? |
| Novelty / white space | 10% | Is it underexplored *right now*? |
| Personal momentum | 5% | Have I already started and stayed interested? |

Scores 1–5; weighted total = Σ(score × weight). Full matrix: `docs/topic-scorecard.md`.

### 1.3 Stress-test the ranking (sensitivity)
Re-weight the model at least three ways (double novelty, double leverage, cut moat) and check whether the winner survives. If the winner changes with weights, the trend is not robust — pick the one that wins under *all* plausible weightings.

### 1.4 Apply hard filters (disqualifiers)
Reject any trend that fails these regardless of score:
- needs a lab, GPU cluster, or funding you do not have;
- needs human subjects / IRB-scale recruitment;
- needs capital-market or US-only data agreements (sanctions/geography);
- needs novel ML theory you cannot supply;
- has no falsifiable question (i.e. it is product work wearing a research costume).

### 1.5 Classify the survivors — one primary, one hedge, the rest absorbed
- **Primary:** highest weighted score, must be the *identity*.
- **Hedge:** second, publishable, low-intensity, must not compete for daily attention.
- **Absorbed:** sub-topics that are instruments/artifacts of the primary.
- **Skip:** everything else, explicitly and on the record.

### 1.6 Write the falsifiable question and the done-criteria *before* starting
No trend is "chosen" until it has (a) a research question, (b) a null hypothesis, (c) acceptance criteria for "done", (d) a pre-registration. See `docs/t1-research-plan.md`.

### 1.7 Re-run the method on a schedule, not on impulse
Re-evaluate quarterly or when a track stalls — never because a new topic looks exciting mid-project. The failure mode this project guards against is dispersion: see §7.

---

## 2. Applied result — the ranked answer

| Rank | Topic | Weighted | Verdict |
|---:|---|---:|---|
| 1 | **T1 Invariant-preserving coding agents** | **4.90** | **Primary track — commit.** |
| 2 | T10 Benchmark harness as open standard | 4.35 | Fold into T1 as its artifact. |
| 3 | T8 Verification / property tests for agent code | 3.95 | Fold into T1 as its instrument. |
| 4 | T3 Runtime guardrails for money movement | 3.90 | Spin-off / product after T1. |
| 5 | T9 Dragon Market as reference architecture | 3.60 | Supporting activity (talks, pedagogy). |
| 6 | T2 Tehran housing × metro accessibility | 3.55 | **Secondary hedge** — one paper. |
| 7 | T7 Persian-language LLM education | 3.45 | Product idea, not a thesis. |
| 8 | T4 LLM repo-quality evaluation | 3.00 | Skip (commodity). |
| 9 | T6 Dev tooling / extension UX research | 2.70 | Build as product only. |
| 10 | T5 Web3 mechanism research | 2.55 | Skip (wrong battlefield). |

**Sensitivity verdict:** T1 stays first when novelty is doubled (4.83), when leverage is doubled (4.95), and when moat is cut to 5% (4.45). The ranking is robust, not an artifact of the weights.

**Per-topic rationales:** T1–T10 detail in §3 below; deeper notes on T2–T10 in `docs/alternatives.md`.

---

## 3. Why T1 wins (the argument in one page)

1. **You can build the target system correctly.** Most agent-evaluation work uses toy or stateless repos. Dragon Market has real invariants — wallet balances, auction close, idempotent payment, reservation expiry — and you wrote it.
2. **The question is crisp and falsifiable.** H0: invariant-oriented guidance does not change the violation rate. H1: it reduces violations without materially reducing task completion.
3. **The artifact outlives the result.** Even a null result leaves a benchmark and harness others can cite and reuse.
4. **It converts into money.** "I build evaluations and guardrails for AI agents touching financial systems" is a premium position in 2026–2027.
5. **It compounds with everything you already have.** Fintech (Nafisagold), Go/Postgres concurrency (Dragon Market), research method (metro-premium), agent tooling (`researchctl`, Kill Switch) — all four feed T1. No other topic uses all four.
6. **It is defensible against bigger labs.** Labs have GPUs and model access; they do not have your production-transaction intuition or your patience for careful, boring benchmarks.

**The concrete framing:** *"SWE-bench measures whether tests pass. It does not measure whether money is conserved."*

---

## 4. The hedge — T2, and why it stays second

`metro-premium` is real, documented, and near-publishable: a 1M-row source audit, 84,586 Tehran listings, a 555,686-node OSM walking graph, a bilingual EN/FA publication, and an honest headline association of **−9.87% per km** with a clustered interval of **−22.85% to +5.28%** and an explicit refusal to claim causality.

It loses on **moat** (urban economics is mature; the method is replicable) and **leverage** (locally valuable, weak global hiring signal), and it will not produce a benchmark. Keep it to **one descriptive paper**, then stop. It is the institutional strong suit for TMU (see §6).

---

## 5. Absorbed and skipped topics

- **T10 harness → artifact of T1.** `researchctl` with provenance, SHA-256 manifests, pinned commits. Give it its own README, version, and citation block.
- **T8 verification → instrument of T1.** Independent state checks, rejected faulty variants, violation taxonomy.
- **T3 guardrails → later product.** Enforcement without measurement is unfounded; T1's taxonomy is T3's policy spec.
- **T9 pedagogy → supporting activity.** Dragon Market explainers double as T1's motivation section; do not let them displace research time.
- **Skip:** T4 (commodity), T5 (needs crypto/mechanism-design depth you do not have), T6 as *research* (ship as product), T7 as *research* (business, not thesis).

---

## 6. Institutional anchor — TMU ISE (faculty research results)

Tarbiat Modares University is the intended home institution. Full note: `docs/tmu-research.md`; raw public pages in `data/ise/` (scraped 2026-10-24 from `ise.modares.ac.ir`, no authenticated pages).

### 6.1 Verdict

**Credible, locally strong anchor — weak direct fit for T1, moderate fit for T2.**

| Anchor role | Composite | Reading |
|---|---:|---|
| T2 (geo/urban data science) | **4.5** | Strong: Socio-economic Systems covers transport planning and regional system design. |
| T1 (invariant-preserving agents) | 3.2 | Secondary: methodology/reliability co-supervision only; no coding-agent subject expertise on the register. |

**Strategy:** T2 → TMU as primary institutional home. T1 → TMU as methodological co-supervisor, with subject expertise sourced externally. Highest-value open gap: check TMU's **Computer Engineering** faculty, which is not covered by the ISE scrape.

### 6.2 Faculty of Industrial & Systems Engineering — structure

Five departments: Industrial Engineering; IT Engineering; Socio-economic Systems; Systems & Productivity Management; Innovation, Entrepreneurship & Learning Systems. Central Campus; `Ise@modares.ac.ir`.

Department managers: **Seyed Hessam-od-Din Zegordi** (Industrial Eng.), **Gholamali Montazer** (IT Eng.), **Majid Sheikh Mohammadi** (Socio-economic Systems), **Bakhtiar Ostadi** (Systems & Productivity Mgmt), **Mohammad Mehdi Sepehri** (Innovation, Entrepreneurship & Learning).

### 6.3 Research-area map (aggregated from the public register)

| Theme cluster | Weight | Representative faculty |
|---|---|---|
| Risk, reliability, resilience, quality | **Very high** (largest) | Bakhtiar Ostadi (~40+ entries), Reza Baradaran Kazemzadeh |
| Financial engineering, banking, portfolio & VaR | **High** | Parastoo Mohammadi, Hamid Banaeian, Mohammad Ali Rastegar, Firouzeh Mokhatab Rafiei |
| Supply chain, logistics, scheduling | **High** | Nasim Nahavandi, Seyed Kamal Chaharsoughi, Zegordi, Ehsan Nikbakhsh |
| Decision analysis, MCDM, optimization | **High** | Ali Hosseinzadeh Kashan, Majid Sheikh Mohammadi, Ehsan Nikbakhsh |
| Data science / ML / NLP / CV / generative AI | **Moderate, growing** | Toktam Khatibi (LLMs, CV, medical imaging), Amir Albadvi (big data), Babak Teimourpour (recommender systems), Elham Akhoundzadeh (data mining) |
| Health systems engineering, e-health, IoT | **Moderate** | Mohammad Mehdi Sepehri, Mehrdad Kargari, Toktam Khatibi |
| Innovation, entrepreneurship, e-learning | **Moderate** | Amir Albadvi, Elham Akbari, Gholamali Montazer |
| Industry 4.0, blockchain, cybersecurity intelligence | **Emerging** | Bakhtiar Ostadi, Motahareh Dehghan |

### 6.4 The decisive finding

- **For T1:** searching the whole register for *software engineering, coding agents, program verification, code generation, agent reliability* returns **nothing**. AI-adjacent work is applied ML (NLP, CV, generative models, recommender systems), not AI-assisted software engineering. TMU ISE cannot supervise T1's core question on subject grounds — only its instrumentation (reliability engineering, experimental design, statistical validation).
- **For T2:** Socio-economic Systems explicitly lists transport planning, AI/ANN forecasting, and urban/regional system design — a direct match to the metro-premium pipeline.

### 6.5 Outreach shortlist

- **T2:** Majid Sheikh Mohammadi, Nasim Nahavandi, Ehsan Nikbakhsh, Ali Hosseinzadeh Kashan.
- **T1 instrumentation:** Bakhtiar Ostadi (reliability/risk), Toktam Khatibi or Babak Teimourpour (data science/validation).

### 6.6 Caveats

Scraped snapshot only; ranks and managers drift, and a register entry is not proof of active funded work. Publication-level checks are required before any commitment. Faculty profile pages follow `pro.modares.ac.ir/pro/academic_staff/<slug>`.

---

## 7. Guardrails (what to stop doing)

- **Stop starting new repos** until T1 has a preprint; repo count is already a dispersion signal.
- **Do not expand metro-premium** beyond one descriptive paper.
- **Do not chase Web3 research**; keep the widget as portfolio only.
- **Do not productise T1** before the pilot report — evaluation first, guardrail product second.
- **Cap context-switching:** one primary track, one hedge, tools only as needed.
- **Re-run §1 on a schedule**, not whenever a shiny topic appears.

---

## 8. Next actions (ordered)

1. Publish the T1 pre-registration (hypotheses, metrics, exclusion rules, analysis plan) — before any run.
2. Harden T001; author T002 (auction close race) and T003 (wallet reservation expiry) with rejected faulty variants.
3. Get one independent reviewer to sign the human baseline — this is the credibility gate.
4. Freeze harness version; pin the Dragon Market commit (`f4ba211…`).
5. Run the 36-run pilot (3 tasks × 2 systems × 2 conditions × 3 reps); the 96-run design is the ceiling, not the target.
6. Write and publish the pilot report + harness release + preprint.
7. Then, and only then, scope the T3 guardrail prototype.

Acceptance for "done": public preprint, public harness, three approved task packages, reproducible pilot report. Nothing less counts.

---

## 9. Files in this repo

| File | Contents |
|---|---|
| `README.md` | This document: the trend-finding method, the ranked answer, and next actions |
| `docs/profile-analysis.md` | Extended evidence table, capability matrix, constraint list, source notes |
| `docs/topic-scorecard.md` | Full scoring matrix, sensitivity analysis, pairwise comparisons |
| `docs/t1-research-plan.md` | Detailed T1 plan: RQs, hypotheses, tasks, threats to validity, timeline, budget |
| `docs/alternatives.md` | Deeper notes and verdicts on T2–T10 |
| `docs/tmu-research.md` | TMU ISE institutional fit: departments, research-areas map, faculty roster, verdict |
| `data/ise/` | Raw public TMU ISE pages backing the institutional note |
| `data/profile-snapshot.json` | Raw GitHub profile snapshot |
| `data/repos-snapshot.tsv` | Repo inventory (name, language, stars, pushed, description) |
| `data/site-notes.md` | Notes from the personal-site extraction |
| `DSH-PRO/` | Tooling incident records (process artefacts, not research content) |

---

*Prepared as an independent evaluation. All claims about the subject derive from public sources: houtanrocky.com and the public GitHub API for `houtanrocky`. No private information was used.*