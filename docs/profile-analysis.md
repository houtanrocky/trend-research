# Extended Profile Analysis

Sources: `https://houtanrocky.com` (fetched 2026-10-24) and the public GitHub REST API for user `houtanrocky` (profile, 93 repos, per-repo READMEs).

## 1. Identity

- **Name:** Houtan Abasi Rocky
- **GitHub:** `houtanrocky`, created 2020-03-28; 90 followers, 88 following; 93 public repos (68 originals, 25 forks); 8 public gists.
- **Site:** houtanrocky.com — "Independent engineer for ambitious products", Tehran, Iran (Remote / On-site).
- **Bio:** "— Development / Design / Strategy — Sweat and grit, not wishful thinking. Sacrifice today for growth tomorrow."
- **Self-description:** Full-Stack Engineer and Technical Lead; 8+ years; 11 selected projects; 5 tools shipped; "scalable, high-performance systems across fintech, AI-driven platforms, Web3, and real-time systems."

## 2. Professional project history (from site)

| Project | Role | Stack | Notes |
|---|---|---|---|
| Nafisagold | Technical Team Lead | NestJS, React, RabbitMQ, Redis, PostgreSQL | Gold-credit platform for Bime Salamat Organization; 4,400 personnel; async credit engine; e-sign; Pasargad PSP. |
| Hidden Bitcoin / Crypto Hunt | Full-Stack Developer | React-Vite, Go, gRPC-Web, Three.js, Web3 | On-chain data via Subsquid/TheGraph; real-time gameplay. |
| Telegram Miner | Full-Stack Developer | React-Vite, Telegram Mini App | Migrated from Next.js to React-Vite "in one night". |
| Breeze.ai | Front-End Developer | React, Firebase | AI-driven gaming image editing platform. |
| Commerceflow.ai | Front-End Developer | React, AI | Generates marketing texts from uploaded images. |
| NeoDrag | Maintainer | TypeScript | Open-source drag-and-drop library; published UML version, core optimizations. |

## 3. Shipped tools (from site)

1. **Session Switcher** (Chrome) — isolated multi-account cookie jars and storage.
2. **Terminal Copy On Select** (VS Code) — native clipboard behavior, no telemetry. 5 stars on GitHub.
3. **Discord Chat Exporter** (Chrome) — portable conversation export.
4. **Udemy Course Insights** (Chrome) — shows original creation dates.
5. **Kill Switch Extension** — privacy-focused extension.

## 4. Research repos (the critical signal)

### 4.1 `agent-invariant-preservation` (Python, created ~2026-10-17)

- Title: **"Preserving Transactional Invariants in AI-Assisted Software Development — An Empirical Study of Coding Agents on Stateful Backend Systems."**
- Researcher: Houtan Rocky, MSc foundation, initial horizon four weeks.
- Research question: *How reliably can coding agents modify stateful backends while preserving existing transactional invariants?*
- Status: explicitly a **planned study**; no empirical results; no validated benchmark tasks yet.
- Infrastructure: `researchctl` CLI, provenance-preserving execution, SHA-256 manifests, synthetic demo data under `.local/demos/`.
- Design ceiling: **8 tasks x 2 agent systems x 2 conditions x 3 repetitions = 96** main-study executions (pilot separate). Explicitly labelled "feasibility ceiling, not a justified sample size."
- Subject system: **Dragon Market** (`houtanrocky/dragon-market`), operational pin `f4ba21185d1ba7b4bbb56f5addcc27d1b75bdec7` (integrates the repaired wallet). Historical baseline `162c5ca` preserved as a failure record.
- Benchmark packages: at least T001 (purchase retries) plus a second; each has references, separate feature/state checks, and rejected faulty variants.
- Known gap: independent human baseline approval **pending**.

**Interpretation:** a genuine, well-scaffolded research program with correct epistemic hygiene (uncertainty, provenance, refusal to overclaim). It is the single strongest asset in the portfolio.

### 4.2 `metro-premium` (Python, created 2026-10-23)

- Title: **"Metro Accessibility and Residential Asking Prices in Tehran: A Network-Based Geospatial Analysis of Public Real Estate Listings."**
- Bilingual EN/FA React publication plus Python pipeline; MIT licence; GitHub Pages site.
- Source audit: entire official Divar CSV = 1,000,000 rows x 60 columns; Tehran apartment-sell = 84,586; with coordinates = 63,126; inside study rectangle = 62,929; missing radius = 43,349; Dec-2024 candidate rows with in-region coordinates and known radius = 3,110.
- Graph: small OSM walking graph 666 nodes / 1,452 directed edges; historical graph 555,686 nodes / 1,236,780 directed edges; retained mapped entrances and routes = 166 / 2,978.
- Exploratory model sample: 2,962 observations across 281 neighborhoods.
- Headline association: **-9.87% per additional km**, neighborhood-clustered interval **-22.85% to +5.28%**; sign flips under location scenarios, therefore **explicitly not an operational premium and not causal**.
- Median asking price in candidate sample: 86.99 M toman/m2 (IQR 58.54-126.67).
- Status: descriptive and exploratory; public metro layers and the primary operational-access claim are **disabled** pending topology and entrance validation.

**Interpretation:** demonstrates that the subject can execute a rigorous, honest empirical study end to end. This methodological credential is what makes T1 credible.

## 5. Engineering assets relevant to research

| Repo | Why it matters |
|---|---|
| `dragon-market` (Go, 2 stars, 17 topics) | The T1 target system: PostgreSQL transactions, auctions, wallets, idempotency, Docker, Testcontainers. |
| `cardtoshaba` (Go) | Full-stack fintech validation and audit-log service; Luhn, ZarinHub, PostgreSQL, Fly.io plus Cloudflare Workers. |
| `uniswap-widget` (TypeScript, 3 stars) | Framework-agnostic Web3 widget with React and Vue bindings. |
| `iranian-banks-react-icons` (TypeScript, 4 stars) | Localization and design-system asset. |
| `vscode-extension-terminalcopyonselect` (JS, 5 stars) | Most-starred repo; developer-tooling craft. |
| `chrome-extension-session-switcher`, `killswitchextension`, `discord-chat-exporter-...` | Consistent ability to ship small, complete, polished tools. |
| `taxio` / Arevan (TypeScript, Next.js) | Persian-language production web app (PostgreSQL, ISR, SEO, Docker). |
| `timer-gamified`, `gamified-life`, `the-musketeers` | Game and gamification instinct; canvas, Svelte. |
| `npmx-utils`, `enforce-houtan-eslint-rule`, `houtan-ts-npm-package` | OSS publishing hygiene. |

## 6. Capability matrix (inferred)

| Capability | Level | Evidence |
|---|---|---|
| Backend / distributed systems | Expert | Dragon Market, Nafisagold |
| PostgreSQL / transactions | Expert | Dragon Market, cardtoshaba |
| Go | Strong | Dragon Market, cardtoshaba |
| TypeScript / React ecosystem | Expert | Many repos plus site projects |
| Python (research) | Intermediate to strong | metro-premium, agent-invariant-preservation |
| Empirical research method | Strong (rare) | metro-premium audits plus agent study design |
| ML / LLM *science* | Beginner to intermediate | Product integrations only; no training or fine-tuning repos |
| Web3 protocol design | Beginner to intermediate | Integration level only |
| Product / UX | Strong | 5 shipped tools |
| Writing / publishing | Emerging | Bilingual site plus research docs |

## 7. Gaps that constrain topic choice

1. **No formal ML or statistics publications yet** — avoid topics requiring novel ML theory.
2. **No lab and no funding** — topics must be runnable solo with commodity APIs.
3. **Breadth over depth** — the topic must *reuse* existing assets, not demand new ones.
4. **Sanctions and geography** — avoid topics requiring capital markets, GPU clusters, or US-only data agreements.
5. **No human-subject infrastructure** — avoid HCI studies needing IRB-scale recruitment; small pilots only.

## 8. What the profile implies strategically

- The **rarest combination** is money-moving production systems plus reproducible research discipline. That intersection is exactly T1.
- The **most crowded** directions are generic web development, generic LLM apps, and generic Web3. Avoid.
- The **highest compounding** asset is a *named benchmark*: it is cited, reused, and remembered. T1 produces one.
- The **biggest risk** is dispersion. The plan must enforce one primary track.

## 9. Source notes

- Site text extracted by stripping scripts, styles, and tags from `https://houtanrocky.com` (57 KB HTML, about 2.5 KB visible text).
- GitHub data: `/users/houtanrocky`, `/users/houtanrocky/repos?per_page=100&sort=updated`, and per-repo `/readme` endpoints.
- Dates reflect the API's reported timestamps; the account `updated_at` is 2026-10-15 and the most recent push observed is 2026-10-23.
- No private repositories, emails, or credentials were accessed.