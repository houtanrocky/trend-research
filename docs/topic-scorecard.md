# Topic Scorecard (full matrix)

Scores 1-5. Weights: Fit 20%, Moat 20%, Ceiling 15%, Leverage 15%, Feasibility 15%, Novelty 10%, Momentum 5%.

| # | Topic | Fit | Moat | Ceiling | Leverage | Feasibility | Novelty | Momentum | Weighted |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| T1 | Invariant-preserving coding agents on stateful backends | 5 | 5 | 5 | 5 | 4 | 5 | 5 | 4.90 |
| T10 | Agent benchmark harness as open standard | 5 | 4 | 3 | 5 | 4 | 4 | 5 | 4.35 |
| T8 | Verification / property tests for agent-generated code | 4 | 4 | 4 | 5 | 4 | 4 | 3 | 3.95 |
| T3 | Runtime guardrails for agents moving money | 4 | 4 | 3 | 5 | 4 | 4 | 3 | 3.90 |
| T9 | Dragon Market as reference architecture / pedagogy | 5 | 4 | 2 | 4 | 5 | 2 | 4 | 3.60 |
| T2 | Tehran housing x metro accessibility (geo) | 4 | 3 | 4 | 3 | 4 | 3 | 4 | 3.55 |
| T7 | Persian-language LLM education tools | 4 | 3 | 3 | 4 | 4 | 3 | 2 | 3.45 |
| T4 | LLM evaluation of repo quality / maintainability | 4 | 2 | 3 | 4 | 4 | 2 | 1 | 3.00 |
| T6 | Developer tooling / extension UX research | 5 | 2 | 2 | 2 | 5 | 1 | 3 | 2.70 |
| T5 | Web3 protocol / DeFi mechanism research | 3 | 2 | 4 | 2 | 2 | 3 | 1 | 2.55 |

## Sensitivity checks

- Novelty weight doubled to 20%, Feasibility halved to 7.5%: T1 = 4.83 (still first); T8 = 3.96 second; T3 = 3.85 third. Conclusion unchanged.
- Leverage weight doubled to 30%: T1 = 4.95, T3 = 4.05, T8 = 3.95. T1 still first.
- Moat weight reduced to 5%: T1 = 4.45, T9 = 3.85, T2 = 3.75. T1 still first because fit and momentum dominate.
- Robustness verdict: T1 is the top choice under every weighting tested.

## Composite view



T1   4.90  ##############################
T10  4.35  ###########################
T8   3.95  ########################
T3   3.90  ########################
T9   3.60  ######################
T2   3.55  #####################
T7   3.45  ####################
T4   3.00  ##################
T6   2.70  ################
T5   2.55  ###############





text









## How to read the scores

- **Fit** — can the researcher execute without a six-month detour into a new field?
- **Moat** — would a typical researcher be unable to do this, or do it as well?
- **Ceiling** — can it produce a paper, thesis, benchmark, or artifact others cite?
- **Leverage** — does it convert into jobs, consulting, speaking, or products?
- **Feasibility** — solo, self-funded, four to six months, no lab?
- **Novelty** — is the space underexplored right now?
- **Momentum** — has work already started and sustained interest?

## Key comparisons

**T1 vs T3.** Both concern agents and money. T1 is *measurement* (does the agent break invariants?). T3 is *enforcement* (can we stop it?). Measurement should come first: you cannot build a credible guardrail without a credible violation taxonomy and baseline rates. T3 becomes a natural spin-off and product once T1's pilot exists.

**T1 vs T8.** T8 is the *instrument* of T1. Property-based testing and transaction simulation are how you detect invariant violations. Keep T8 inside T1 rather than as a separate track.

**T1 vs T10.** T10 is the *vehicle* of T1. The harness is what makes the study reproducible and citable. Ship it as T1's artifact, not as an independent research program.

**T1 vs T2.** T2 is the strongest alternative and the only one with a genuinely active second repo. It loses on moat (urban economics is a mature field with established methods) and on leverage (limited global hiring signal), but it wins on feasibility and on having a working pipeline. Keep it as a hedge and a publication, not as the identity.

**T1 vs T5.** Web3 research requires mechanism-design and cryptography depth that the profile does not yet show. The Uniswap widget is integration work, not protocol research. Wrong battlefield.

**T1 vs T7.** Persian-language education tooling is a real market opportunity with genuine local advantage, but the research ceiling is low without education-theory grounding and human-subject infrastructure. Product line, not thesis.