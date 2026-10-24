# Alternatives — Detailed Notes on T2 to T10

This document expands on the topics that were scored but not chosen as the primary track. It is meant to be read when the main track stalls or when a second parallel effort is justified.

---

## T2. Geo-Spatial Housing and Accessibility Analysis (metro-premium line)

**Status:** active repo, well documented, publication near-ready.

**What exists:** a 1,000,000-row source audit of the Divar dataset, a filtered Tehran apartment sample (84,586 listings, 63,126 with coordinates, 3,110 candidates in the December 2024 window), an OSM walking graph (555,686 nodes, 1,236,780 edges), 166 retained mapped entrances and 2,978 supported routes, and an exploratory model sample of 2,962 observations across 281 neighborhoods. Bilingual EN/FA publication is already built.

**What is missing:** independent metro topology validation, entrance completeness checks, and historical operation verification. Those are precisely the items the repo disables its public claims over.

**Why it is second, not first:**
- **Moat is low.** Urban economics has an established toolkit: hedonic regressions, accessibility indices, spatial clustering. A competent urban-economics researcher could replicate the method; what they could not easily get is the local data access and the willingness to report uncertainty this honestly.
- **Leverage is local.** The output is valuable to Iranian policy, real-estate, and academic audiences. It does not translate into a global hiring or consulting signal the way agent-safety work does.
- **Ceiling is real but bounded.** It is publishable in applied geo and urban venues, and the bilingual framing is genuinely distinctive. But it will not produce a *benchmark* that others adopt.

**Recommended scope if pursued:**
Finish exactly one deliverable — a defensible *descriptive* paper titled along the lines of "What public listing data can and cannot tell us about metro accessibility in Tehran." Report the -9.87% per km association with its -22.85% to +5.28% clustered interval, state clearly that sign flips under location scenarios, and refuse to make causal claims. Then stop.

**Do not:** chase causal identification, expand to other cities, or build a product on top of a dataset whose publisher terms are unclear.

---

## T3. AI Agent Guardrails and Runtime Policy Enforcement for Money Movement

**The question:** can a runtime policy layer provably constrain what an autonomous agent may do to a financial system?

**Why it is attractive:** highest commercial leverage of any topic on the list. "Agent safety for fintech" is a live budget line in 2026-2027. The Kill Switch extension is a proof that you can build enforcement mechanisms, not just evaluation harnesses.

**Why it is not first:**
- **Enforcement without measurement is unfounded.** You cannot specify what a guardrail should block without knowing which violations agents actually produce. That is T1's descriptive output.
- **Research ceiling is engineering-paper level.** A strong systems artifact, less of a scientific result.
- **Premature productisation risk.** Building the guardrail before the pilot report would invert the epistemics: you would be motivated to find violations.

**How it should unfold:** T1 phase 3 produces the violation taxonomy and baseline rates. T3 then takes that taxonomy as its policy specification and builds enforcement. The findings determine the design, not the reverse.

---

## T4. LLM-Based Evaluation of Repository Quality and Maintainability

**The idea:** use LLMs to score repo maintainability, test quality, and architectural risk, validated against human reviewers.

**Why it scores low:** the space is saturated. CodeRabbit, Snyk, Sonar, and a substantial academic literature on code metrics all occupy it. A metric-validation paper is publishable but low prestige, and there is no obvious moat: any competent team can build the same tool.

**Verdict:** skip. If you want a lightweight version, fold a repo-quality check into the T1 harness as an auxiliary signal, not as a research question.

---

## T5. Web3 Protocol and DeFi Mechanism Research

**The idea:** study swap routing, MEV, AMM design, or on-chain data pipelines.

**Why it scores lowest:**
- **Wrong depth.** The Uniswap widget is integration work: React and Vue bindings around an existing core. Protocol research requires mechanism design, game theory, and cryptography depth that the profile does not demonstrate.
- **Market and geography friction.** Iranian sanctions complicate participation in global crypto-research roles and funding.
- **Crowded.** The field is dense with well-funded specialists.

**Verdict:** keep the widget as a portfolio piece. Do not enter mechanism-design research.

---

## T6. Developer Tooling and Browser-Extension UX Research

**The idea:** measure the developer-productivity impact of extensions like copy-on-select or session switcher.

**Reality check:** this is not a research field. The best available venue is an HCI workshop with n=10, which is a blog post with extra steps. The 5-star Terminal Copy On Select repo is a genuine achievement *as a product*; treat it as one.

**Verdict:** continue shipping tools. Do not frame them as research.

---

## T7. LLM-Assisted Education and Localized Learning Tools (Persian)

**The idea:** adaptive learning, Persian-language educational tooling, Udemy-insight-style products.

**Strengths:** the Persian-language market is genuinely underserved, there is real monetisation potential, and the profile shows relevant instincts (Udemy helper repos, teaching orientation).

**Weaknesses as research:** learning-analytics venues (LAK, AIED) require education-theory grounding and human-subject infrastructure. Without those, the work is product development, not research.

**Verdict:** a legitimate business idea. If pursued, pursue it as a product with user research, not as a thesis. It also competes for attention with T1, which is the greater risk.

---

## T8. Reliability Engineering for AI-Generated Code (Verification)

**The idea:** can static analysis, property-based tests, and transaction simulators catch agent-introduced bugs before merge?

**Relationship to T1:** this is T1's *instrument*. The independent state checks, the rejected faulty variants, and the violation taxonomy are all T8 content. Keeping T8 as a separate track would duplicate effort and split attention.

**Verdict:** fold into T1. Publish the verification machinery as part of the harness release. If the pilot reveals that verification *alone* catches most violations, that becomes an additional finding inside the T1 paper, not a separate study.

---

## T9. Distributed Systems Pedagogy and Reference Architectures

**The idea:** turn Dragon Market into a teaching reference for concurrency, idempotency, and wallet design.

**Strengths:** high ROI, nearly done already, and reputation-building. Talks, courses, and hiring conversations all benefit. The Testcontainers-plus-idempotency focus is a genuine differentiator among reference repos.

**Weakness:** it is not research. There is no hypothesis, no measurement, no contribution to knowledge.

**Verdict:** run it as a *supporting activity* alongside T1. A good explainer of Dragon Market's transaction design doubles as the motivation section of the T1 paper. Do not let it displace research time.

---

## T10. AI Coding Agent Benchmark Infrastructure as an Open Standard

**The idea:** release `researchctl` and the benchmark format as a reusable standard for stateful-agent evaluation.

**Why it scores high:** early mover, real utility, and standards confer authority. Few stateful-agent harnesses exist.

**Why it is not a standalone track:** infrastructure papers are cited but are not the headline result. The value of the harness comes from what it measures, which is T1.

**Verdict:** ship the harness as T1's artifact. Give it its own README, its own version number, and its own citation block. That is sufficient.

---

## Summary table

| Topic | Standalone? | Fold into T1? | Support activity? | Skip? |
|---|---|---|---|---|
| T2 metro-premium | Yes (one paper) | No | Yes (low intensity) | No |
| T3 guardrails | No (after T1) | No | Product spin-off | Not yet |
| T4 repo-quality LLM eval | No | Auxiliary signal only | No | Yes |
| T5 Web3 mechanism research | No | No | Portfolio only | Yes |
| T6 dev tooling UX research | No | No | Ship as product | Research: yes |
| T7 Persian LLM education | Business, not research | No | Possible later | As research: yes |
| T8 verification | No | **Yes, core** | — | No |
| T9 Dragon Market pedagogy | No | Motivation material | Yes | No |
| T10 harness standard | No | **Yes, artifact** | — | No |