# Tarbiat Modares University — Finalized Research Note

**Prepared:** 2026-10-24
**Scope:** Faculty of Industrial & Systems Engineering (دانشکده مهندسی صنایع و سیستم‌ها), Tarbiat Modares University (TMU)
**Evidence base:** `data/ise/` — scraped public pages from `ise.modares.ac.ir` (departments, research areas, faculty list, group managers). No private or authenticated pages accessed.
**Purpose:** Decide whether TMU/ISE is a viable institutional anchor (supervision, co-authorship, or affiliation) for the primary track T1 (Invariant-Preserving Coding Agents) and the secondary track T2 (metro-premium geo research).

---

## 1. Executive verdict

**TMU ISE is a credible, locally strong anchor — but a weak direct fit for T1 and a moderate fit for T2.**

- The faculty's strength is **operations research, reliability/resilience engineering, financial engineering, data science, and supply-chain/risk modeling**. That is deep, mature, well-populated expertise.
- The faculty's **AI-systems / software-engineering research surface is thin**: the AI-adjacent work that exists is *applied ML* (NLP, computer vision, generative models, recommender systems), not *AI-assisted software engineering* or *agent reliability*.
- **Recommendation:** treat TMU ISE as the **institutional home for T2 (geo/urban data science)** and as a **secondary co-supervision path** for T1 — specifically through the **reliability/resilience and data-science faculty**, who can legitimately co-supervise a study about *verification of agent-generated code against invariants*. Do **not** expect TMU to supply T1 domain expertise in coding agents; that must come from the external/industry side and from the agent-invariant-preservation program itself.

---

## 2. Institutional facts (from the scraped pages)

| Item | Detail |
|---|---|
| Faculty | دانشکده مهندسی صنایع و سیستم‌ها (Faculty of Industrial & Systems Engineering) |
| Site | `ise.modares.ac.ir` (Esprit Portal 3.1.39) |
| Contact | `Ise@modares.ac.ir`, phones 82884393 / 82884323 / 82884386, fax 82884393 |
| Location | Central Campus (پردیس مرکزی) |
| Departments (5) | Industrial Engineering; IT Engineering; Socio-economic Systems; Systems & Productivity Management; Innovation, Entrepreneurship & Learning Systems |

### 2.1 Departments and their stated scope

1. **Industrial Engineering** — design/improvement of integrated human–material–equipment–energy–information systems; MSc: Industrial Engineering, Healthcare Systems Engineering; PhD: Industrial Engineering.
2. **IT Engineering** (est. 1382 / ~2003) — MSc: IT Systems, Networked Systems; PhD: Information Systems Management.
3. **Socio-economic Systems** — planning/design of large national and regional systems: transport, water/wastewater, communications, goods distribution, energy, education/health services.
4. **Systems & Productivity Management** (est. 1377 / ~1998) — MSc tracks in Engineering Management and Financial Engineering.
5. **Innovation, Entrepreneurship & Learning Systems** — historically ran a joint program with Luleå University of Technology (Sweden), 1382–85, graduating ~130 students.

**Reading:** departments 3 and 4 are the closest institutional match to the researcher's fintech/transactional background (financial engineering, socio-economic systems), while department 2 is the closest match to the data/AI side.

### 2.2 Department managers

| Department | Manager |
|---|---|
| Industrial Engineering | Seyed Hessam-od-Din Zegordi (سیدحسام الدین ذگردی) |
| IT Engineering | Gholamali Montazer (غلامعلی منتظر) |
| Innovation, Entrepreneurship & Learning Systems | Mohammad Mehdi Sepehri (محمدمهدی سپهری) |
| Socio-economic Systems | Majid Sheikh Mohammadi (مجید شیخ محمدی) |
| Systems & Productivity Management | Bakhtiar Ostadi (بختیار استادی) |

---

## 3. Research-areas map (the decisive section)

The faculty publishes a research-areas register with **title + faculty member + rank + department**. Aggregated by theme, the distribution is heavily skewed:

| Theme cluster | Relative weight in the register | Representative faculty |
|---|---|---|
| Risk, reliability, resilience, quality, process excellence | **Very high** (largest single cluster) | Bakhtiar Ostadi (dominant, ~40+ entries), Reza Baradaran Kazemzadeh |
| Financial engineering, banking, Islamic finance, portfolio & VaR | **High** | Parastoo Mohammadi, Hamid Banaeian, Mohammad Ali Rastegar, Firouzeh Mokhatab Rafiei |
| Supply chain, logistics, production planning, scheduling | **High** | Nasim Nahavandi, Seyed Kamal Chaharsoughi, Zegordi, Ehsan Nikbakhsh |
| Data science / big data / ML / NLP / CV / generative AI | **Moderate and growing** | Toktam Khatibi (NLP, CV, LLMs, medical imaging), Amir Albadvi (big data, social networks), Babak Teimourpour (data science, recommender systems), Elham Akhoundzadeh (data mining, complex networks) |
| Decision analysis, multi-criteria, optimization, robust/stochastic programming | **High** | Ali Hosseinzadeh Kashan, Majid Sheikh Mohammadi, Ehsan Nikbakhsh, Nasim Nahavandi |
| Health systems engineering, e-health, IoT in health | **Moderate** | Mohammad Mehdi Sepehri, Mehrdad Kargari, Toktam Khatibi |
| Innovation ecosystems, entrepreneurship, learning systems, e-learning | **Moderate** | Amir Albadvi, Elham Akbari, Gholamali Montazer |
| Industry 4.0, IoT, blockchain, cybersecurity intelligence | **Low-to-moderate, emerging** | Bakhtiar Ostadi (Industry 4.0), Motahareh Dehghan (blockchain/IoT, AI for cybersecurity) |

### 3.1 The signal that matters for T1

Searching the entire research register for **software engineering, coding agents, program verification, code generation, or agent reliability** yields **nothing**. The closest entries are:

- «هوشمندی امنیت سایبری» — AI (evolutionary algorithms, ML, RL) applied to cybersecurity problems (Motahareh Dehghan).
- «مدلهای بزرگ زبانی و کوچک» / «هوش مولد» — LLMs and generative models (Toktam Khatibi), framed as *applied modeling*, not as software-engineering methodology.
- «تحلیل و واکاوی سیگنالهای فیزیولوژیک», «واکاوی تصاویر پزشکی» — applied ML in health.

**Conclusion:** TMU ISE would not be able to supervise T1's core question (do agents preserve transactional invariants?) on subject-matter grounds. It *can* supervise the **instrumentation** side — reliability engineering, statistical validation, experimental design, risk modeling — which is genuinely valuable and complements the plan's `docs/t1-research-plan.md` credibility gate.

### 3.2 The signal that matters for T2

The Socio-economic Systems department explicitly lists **transport planning, forecasting with AI/neural networks, urban/regional system design** — and the late Mohammad Reza Amin Naseri's registered area was *transport planning with AI/ANN forecasting*. Combined with the researcher's `metro-premium` pipeline (Tehran listings × metro accessibility × OSM graph), this is a **strong institutional fit**: the department's stated purpose is exactly large-scale regional/national system planning.

---

## 4. Faculty roster (current, from `faculty-members.html`)

Names, ranks and departments as published. Useful for outreach targeting.

| Name | Rank | Department |
|---|---|---|
| Elham Akhoundzadeh Noghani | Assistant Prof. | IT Engineering |
| Bakhtiar Ostadi | Professor | Systems & Productivity Mgmt |
| Mohammad Aghdasi | Professor | Systems & Productivity Mgmt |
| Amir Albadvi | Professor | IT Engineering |
| Elham Akbari | Associate Prof. | Innovation, Entrepreneurship & Learning |
| Hamid Banaeian | Assistant Prof. | Systems & Productivity Mgmt |
| Sara Bourbour Hossein Beigi | Assistant Prof. | IT Engineering |
| Babak Teimourpour | Associate Prof. | IT Engineering |
| Seyed Kamal Chaharsoughi | Professor | Industrial Engineering |
| Ali Hosseinzadeh Kashan | Associate Prof. | Socio-economic Systems |
| Toktam Khatibi | Associate Prof. | Industrial Engineering |
| Motahareh Dehghan Chachkami | Assistant Prof. | IT Engineering |
| Seyed Hessam-od-Din Zegordi | Professor | Industrial Engineering |
| Mohammad Ali Rastegar Sorkheh | Associate Prof. | Systems & Productivity Mgmt |
| Mohammad Mehdi Sepehri | Professor | Industrial Engineering |
| Majid Sheikh Mohammadi | Associate Prof. | Socio-economic Systems |
| Faraz Salehi | Assistant Prof. | Industrial Engineering |
| Mohammad Reza Ghatreh Samani | Assistant Prof. | Industrial Engineering |
| Parastoo Mohammadi | Assistant Prof. | Systems & Productivity Mgmt |
| Gholamali Montazer | Professor | IT Engineering |
| Nasim Nahavandi | Professor | Socio-economic Systems |
| Ehsan Nikbakhsh | Assistant Prof. | Socio-economic Systems |
| Mehrdad Kargari | Associate Prof. | IT Engineering |
| Elham Yavari | — | (listed) |
| Reza Baradaran Kazemzadeh | Professor (retired) | Systems & Productivity Mgmt |
| Firouzeh Mokhatab Rafiei | Associate Prof. (retired) | Systems & Productivity Mgmt |
| Mohammad Reza Amin Naseri | Professor (deceased) | Socio-economic Systems |

Profile pages follow the pattern `https://pro.modares.ac.ir/pro/academic_staff/<slug>` (slugs captured in `data/ise/it-staff-links.txt`).

---

## 5. Fit assessment against the research program

Scored 1–5, using the same criteria as `docs/topic-scorecard.md`.

### 5.1 TMU ISE as anchor for T1 (Invariant-Preserving Coding Agents)

| Criterion | Score | Rationale |
|---|---:|---|
| Subject-matter fit | 2 | No software-engineering / coding-agent / program-verification expertise on the register. |
| Methodological fit | 4 | Reliability engineering, experimental design, statistical validation, risk modeling are directly usable for the benchmark's credibility gate. |
| Supervision availability | 3 | Reliability/resilience and data-science faculty could co-supervise the *instrument*; the *subject* needs an external supervisor. |
| Institutional prestige (local) | 5 | TMU is among Iran's most selective graduate institutions. |
| Institutional prestige (global, in this subfield) | 2 | Not a recognized venue-producing center for AI-SE research. |
| Access / logistics | 5 | Local, same city, Persian-language, existing relationship surface. |
| **Composite** | **3.2** | Viable as a *secondary* anchor, not the primary one. |

### 5.2 TMU ISE as anchor for T2 (Tehran housing × metro accessibility)

| Criterion | Score | Rationale |
|---|---:|---|
| Subject-matter fit | 4 | Socio-economic Systems department explicitly covers transport planning, regional system design, AI-based forecasting. |
| Methodological fit | 5 | Optimization, spatial/statistical modeling, DEA, simulation are all in-house. |
| Supervision availability | 4 | Multiple faculty in Socio-economic Systems and Industrial Engineering. |
| Institutional prestige (local) | 5 | Same as above. |
| Data access | 4 | Local institutional access to urban/transport data is plausible via the department. |
| Access / logistics | 5 | Local. |
| **Composite** | **4.5** | **Best institutional match of the two tracks.** |

---

## 6. Concrete actions

Ordered, with acceptance criteria.

1. **Pick the outreach targets.**
   - For T2: Majid Sheikh Mohammadi (Socio-economic Systems manager), Nasim Nahavandi, Ehsan Nikbakhsh, Ali Hosseinzadeh Kashan.
   - For T1 instrumentation: Bakhtiar Ostadi (reliability/resilience/risk), Toktam Khatibi or Babak Teimourpour (data science / validation).
   - *Done when:* a shortlist of 2–3 names per track is written down with the specific research hook for each.

2. **Prepare a one-page bilingual brief per track.**
   - T2 brief: metro-premium pipeline summary + the research question + what TMU supervision would add (spatial methods, transport data access).
   - T1 brief: invariant-preservation benchmark summary + the explicit request for *methodological* co-supervision (experimental design, reliability metrics, statistical validation), not subject supervision.
   - *Done when:* both briefs exist as PDFs/Markdown and are reviewed for accuracy against `docs/t1-research-plan.md` and the metro-premium materials.

3. **Verify the open questions against primary sources.**
   - Confirm current department managers and faculty ranks on `pro.modares.ac.ir` (the scraped pages may lag reality).
   - Confirm admission/co-supervision rules for the intended program (the scraped data says nothing about this).
   - Confirm whether the Socio-economic Systems department has active transport/urban projects.
   - *Done when:* each open question has a dated source or is explicitly marked "unverified".

4. **Decide the institutional strategy.**
   - Recommended: **T2 → TMU as primary institutional home**; **T1 → TMU as secondary methodological co-supervisor, with subject expertise sourced elsewhere**.
   - *Done when:* the decision is recorded in `README.md` and the `docs/alternatives.md` comparison is updated.

---

## 7. Limitations and what would change the verdict

- **Scraped snapshot only.** All findings come from public `ise.modares.ac.ir` pages captured 2026-10-24. Faculty ranks, managers and research areas change; nothing here was cross-checked against `pro.modares.ac.ir` profiles or the university's central site.
- **Register ≠ activity.** A research area listed on a page does not prove active funding, current students, or recent publications in that area. Publication-level verification is required before any commitment.
- **One faculty, not the whole university.** TMU's Computer Engineering department (a different faculty) is not covered here and could be a much better T1 anchor — this is the single highest-value gap to close next.
- **Would change the verdict if:** (a) TMU's Computer Engineering faculty has software-engineering/SE-for-AI researchers, or (b) ISE has an unlisted active program in AI-assisted software development. Either would raise T1's institutional fit substantially.

---

## 8. Sources

All from `data/ise/` (public pages, `ise.modares.ac.ir`):

- `departments.html` — the five departments and their stated scope.
- `department-managers.html` — current department managers.
- `research-areas.html` — the research-areas register (title, faculty, rank, department).
- `faculty-members.html` — current, retired and former faculty lists.
- `it-staff-links.txt` — profile URL slugs on `pro.modares.ac.ir`.
- `extracted-fa.txt` — consolidated Persian text of the above pages.