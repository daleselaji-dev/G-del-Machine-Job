# Job Requirements Database

status: ACTIVE_WORKING_MAP  
version: v0.1  
created_at: 2026-06-28  
last_updated: 2026-06-28  
purpose: collect target-JD requirements, hidden capability demands, candidate evidence mapping, skill gaps and training actions  
related: `CAREER_EVIDENCE_DATABASE.md`

> This file stores job requirements, not resume prose. A target resume selects supported evidence from the career database against the requirements recorded here.

## 1. Maintenance rules

- Preserve the original JD wording whenever available.
- Separate `JD_FACT`, `ROLE_INFERENCE`, `COMPANY_CONTEXT` and `UNKNOWN`.
- Do not convert a common role-family expectation into an exact claim about a specific job.
- One job gets one stable `JREQ` ID, even if its title or page changes.
- Update the current requirement map without deleting meaningful historical requirements.
- Record why a job was discovered or missed so retrieval policy can improve.
- Major resume claims must link to evidence IDs in `CAREER_EVIDENCE_DATABASE.md`.

### Status vocabulary

| Status | Meaning |
|---|---|
| `LINK_CAPTURED` | Link and platform are recorded. |
| `JD_TEXT_PENDING` | Exact page text is not yet available. |
| `JD_VERIFIED` | Exact responsibilities and requirements were captured. |
| `CAPABILITY_MAPPED` | Hidden capability tree was extracted. |
| `EVIDENCE_MAPPED` | Candidate evidence and gaps were mapped. |
| `APPLIED` | Candidate confirmed application. |
| `INTERVIEW_FEEDBACK` | Interview evidence has been added. |
| `CLOSED` | Role closed or no longer actionable. |

## 2. Current Zhipu target-role registry

### JREQ-ZHIPU-001 — Moka role UUID `4aea2eaf-2c0e-4e2e-bd03-69a9576d1c84`
- **Source:** Moka social recruitment, Zhipu organization `zphz`, site `148983`.
- **URL:** https://app.mokahr.com/social-recruitment/zphz/148983?locale=zh-CN#/job/4aea2eaf-2c0e-4e2e-bd03-69a9576d1c84
- **Status:** `LINK_CAPTURED + JD_TEXT_PENDING`
- **Title/location/department:** `UNKNOWN` until exact JD text or screenshot is captured.
- **Do not infer:** role family solely from prior search history.

### JREQ-ZHIPU-002 — Moka role UUID `1cf4751d-16d1-4ff9-bc56-e3eb7617f2cc`
- **Source:** Moka social recruitment, Zhipu organization `zphz`, site `148983`.
- **URL:** https://app.mokahr.com/social-recruitment/zphz/148983?locale=zh-CN#/job/1cf4751d-16d1-4ff9-bc56-e3eb7617f2cc
- **Status:** `LINK_CAPTURED + JD_TEXT_PENDING`
- **Title/location/department:** `UNKNOWN`.

### JREQ-ZHIPU-003 — Moka role UUID `14e29409-d54a-424f-8f39-560bca47e81d`
- **Source:** Moka social recruitment, Zhipu organization `zphz`, site `148983`.
- **URL:** https://app.mokahr.com/social-recruitment/zphz/148983?locale=zh-CN#/job/14e29409-d54a-424f-8f39-560bca47e81d
- **Status:** `LINK_CAPTURED + JD_TEXT_PENDING`
- **Title/location/department:** `UNKNOWN`.

### JREQ-ZHIPU-004 — BOSS shared role `fac829d2d8da29900nZ73dq6E1NS`
- **URL:** https://m.zhipin.com/mpa/html/weijd/weijd-job/fac829d2d8da29900nZ73dq6E1NS
- **Status:** `LINK_CAPTURED + JD_TEXT_PENDING`
- **Title/location:** `UNKNOWN`.

### JREQ-ZHIPU-005 — BOSS shared role `5819e45d8b3cb5a40nR_29u4EVpX`
- **URL:** https://m.zhipin.com/mpa/html/weijd/weijd-job/5819e45d8b3cb5a40nR_29u4EVpX
- **Status:** `LINK_CAPTURED + JD_TEXT_PENDING`
- **Title/location:** `UNKNOWN`.

### JREQ-ZHIPU-006 — BOSS shared role `1f36b716e431de2303152d6_F1NT`
- **URL:** https://m.zhipin.com/mpa/html/weijd/weijd-job/1f36b716e431de2303152d6_F1NT
- **Status:** `LINK_CAPTURED + JD_TEXT_PENDING`
- **Title/location:** `UNKNOWN`.

### User-supplied role identity pending URL mapping
- One of `JREQ-ZHIPU-004..006` is a **Malaysia overseas-sales role** and is a current candidate priority.
- Exact URL-to-title mapping must be confirmed from the page text or screenshot before the role is marked `JD_VERIFIED`.

## 3. Why the previous search missed these roles

### Failure F-001 — Hash-routed ATS pages
- The Moka URLs store the job UUID after `#`.
- URL fragments are handled by the browser and are not part of the normal server request or search-engine index key.
- Multiple jobs therefore appear externally as the same recruitment homepage unless the crawler executes the application and its job-detail request.
- **Repair:** whenever a company uses a SPA/ATS, enumerate the official career portal or ingest user-supplied job links directly; do not rely on indexed title search alone.

### Failure F-002 — JavaScript shell and protected job API
- The visible page is a JavaScript application rather than a server-rendered JD.
- Moka documents job-detail endpoints, but its Open API uses organization credentials/API authorization; ordinary public search does not expose each UUID as an indexed page.
- **Repair:** mark a supplied link as `DISCOVERED` even when the body cannot be extracted; request a screenshot/text export rather than concluding the role is absent.

### Failure F-003 — BOSS mobile share links
- BOSS links are mobile share pages with opaque job IDs and session/query parameters.
- They are poor discovery sources for general web search and may resist non-browser retrieval.
- **Repair:** include BOSS as a direct/manual intake channel, store the stable job path/ID, and capture the JD text at discovery time.

### Failure F-004 — Title-led query design
- Earlier retrieval emphasized known titles such as MaaS solution, industry BD, ecosystem or large-model sales.
- A valid role may use a different title while requiring the same responsibilities.
- **Repair:** search by responsibility clusters: market entry, partner recruitment, solution discovery, API commercialization, PoC, customer success, internationalization, localization and enterprise account development.

### Failure F-005 — Location bias
- The active search emphasized Shanghai/Hangzhou/Yangtze River Delta.
- Malaysia or overseas-posted positions can be excluded before capability matching.
- **Repair:** run a separate international-location pass for target companies and accept travel/relocation roles into `WATCH` before applying the user constraint gate.

### Failure F-006 — No durable user watchlist
- Candidate-discovered jobs were not previously captured as first-class objects.
- **Repair:** every user-supplied link receives a stable `JREQ` entry, extraction status and next action even when current tools cannot read it.

## 4. Zhipu company/product context relevant to commercial roles

### CTX-ZHIPU-001 — MaaS and developer platform
- **Type:** `COMPANY_CONTEXT`
- The BigModel platform presents model APIs plus Agent, web search, MCP, knowledge base and fine-tuning capabilities.
- Its official documentation positions the platform as a one-stop MaaS environment covering model/application development, inference and evaluation.
- **Commercial implication:** a Zhipu seller or solutions role is unlikely to be simple license sales. It may require scenario diagnosis, model/API selection, PoC design, token/cost discussion, integration, deployment and post-sale adoption.

### CTX-ZHIPU-002 — Enterprise solution fields
- **Type:** `COMPANY_CONTEXT`
- Official enterprise materials describe intelligent terminals, intelligent manufacturing, consumer applications and partner programs.
- **Commercial implication:** role performance may depend on vertical-industry discovery, ecosystem cooperation and converting model capabilities into measurable workflows.

### CTX-ZHIPU-003 — Malaysia/sovereign-AI direction
- **Type:** `COMPANY_CONTEXT + ROLE_INFERENCE`
- Public reporting describes Zhipu activity in Malaysia and other emerging markets around localized or sovereign-AI infrastructure.
- **Implication, not exact JD fact:** a Malaysia sales role may involve government/large-enterprise stakeholders, local integrators/cloud/hardware partners, multilingual localization, private or sovereign deployment, data control and long-cycle project coordination.
- Do not present these as the exact responsibilities until the JD is captured.

## 5. Preliminary capability model — Malaysia overseas sales

> This section is a role-family hypothesis based on the user-identified title and Zhipu's product/business context. It is not a substitute for the exact JD.

### C1. New-market entry
- Build a Malaysia account and ecosystem map.
- Segment government, state-linked enterprises, large private enterprises, universities, developers, cloud/data-center partners, system integrators and distributors.
- Identify entry route: direct enterprise, government project, strategic partner or developer ecosystem.
- **Candidate evidence:** `MG-001`, `MG-003`, `FF-001`.
- **Current strength:** strong transferable evidence.

### C2. Enterprise/solution discovery
- Discover business workflow, data, model, deployment, integration and success-metric requirements.
- Translate broad AI interest into a specific use case and buying case.
- **Candidate evidence:** `MG-002`, `MG-005`, `FF-002`, `FF-007`, `BENY-001`.
- **Current strength:** technical-product translation exists; formal AI discovery artifacts are missing.

### C3. MaaS/API commercial literacy
- Understand model/API capabilities, context/token usage, price and cost logic, latency/concurrency, fine-tuning, knowledge bases, Agent/tool use, evaluation and service levels.
- Explain cloud API versus private/on-premises/sovereign deployment at a commercial level.
- **Candidate evidence:** `TOOL-003` only as learning status.
- **Gap:** high-priority proof gap.

### C4. PoC and technical-sales coordination
- Define PoC scope, dataset/input, baseline, success criteria, timeline, owner and go/no-go decision.
- Coordinate model, solution, delivery, security and customer teams.
- **Candidate evidence:** `MG-005`, `FF-007` as transferable coordination.
- **Gap:** no formal AI PoC artifact yet.

### C5. Partner/ecosystem development
- Recruit and qualify local integrators, cloud/hardware partners, implementation partners and strategic channels.
- Define joint pipeline, enablement, ownership, incentives and delivery boundaries.
- **Candidate evidence:** `MG-001`, `MG-003`, `MG-004`, `FF-005`.
- **Current strength:** one of the strongest fit areas.

### C6. Complex account and commercial execution
- Navigate multiple decision makers, procurement, legal, security, deployment, payment and acceptance.
- Defend value against lower price or competing models.
- **Candidate evidence:** `MG-002`, `MG-005`, `FF-003`, `FF-005`.
- **Current strength:** good value-selling and coordination evidence; tender/government evidence needs verification.

### C7. Localization and cross-cultural communication
- Work in English with local stakeholders and adapt proposals, materials, demos and partner enablement.
- Malaysia may require sensitivity to English, Malay and Chinese business contexts.
- **Candidate evidence:** `BENY-001`, `BENY-002`, `FF-006`, `EDU-001` plus English negotiation evidence.
- **Gap:** no confirmed Malaysia-specific network or Malay-language ability.

### C8. Market and competitor intelligence
- Track local AI policy, data residency, cloud/compute ecosystem, local models, open-source alternatives, multinational competitors and pricing.
- **Candidate evidence:** `MG-003`, `FF-001`.
- **Current strength:** strong research foundation; AI competitive map needs a demonstrable sample.

### C9. Security, compliance and sovereign-AI literacy
- Discuss data location, privacy, model ownership/control, deployment boundaries, security review and local compliance without overclaiming legal expertise.
- **Candidate evidence:** none direct.
- **Gap:** targeted learning required.

### C10. Field ownership
- Travel or relocate, run pipeline independently, forecast, report and coordinate across time zones.
- **Candidate evidence:** overseas region ownership, English calls/visits, order and delivery coordination.
- **Need confirmation:** willingness to be based in Malaysia, travel frequency and compensation expectations.

## 6. Preliminary candidate fit — Malaysia route

| Capability | Fit | Evidence | Main risk |
|---|---|---|---|
| 0→1 market entry | Strong transferable | MG-001, MG-003 | India/channel context, not Malaysia AI |
| Channel/partner sales | Strong | MG-001, MG-003, FF-005 | local SI/cloud ecosystem vocabulary |
| English commercial communication | Strong | FF-005, FF-002 | live AI demo/technical Q&A evidence |
| Value selling | Strong | MG-002 | API/model ROI case missing |
| Account intelligence | Strong | FF-001, MG-003 | Malaysia target-account map missing |
| Cross-functional delivery | Medium-strong | MG-005, FF-007 | no AI PoC/deployment artifact |
| Localization | Medium | MG-004, FF-006, BENY-002 | Malaysia-specific localization missing |
| MaaS/API knowledge | Early | TOOL-003 | major screening/interview gap |
| AI solution design | Early-transferable | BENY-001, MG-005 | no formal solution architecture/PoC |
| Security/compliance | Weak | none direct | sovereign-AI/data-residency literacy |
| B2G/tender | Unknown | MG-006 pending | evidence scope not confirmed |

### Preliminary recommendation
- Treat the Malaysia role as a **high-value transition role**, not a pure direct-fit sales role.
- Apply if the exact JD does not impose a hard requirement for prior AI/cloud sales, local Malaysian network, Malay fluency or many years of government-account experience.
- The resume should lead with market entry, channel construction, technical-product ramp, value selling and complex coordination—not generic overseas sales.

## 7. Exact-JD extraction template

For each role, fill:

```text
JREQ ID:
Exact title:
Company/legal entity:
Platform and checked date:
Location / relocation / travel:
Employment type:
Experience / education / language:

Original responsibility 1:
- Observable output:
- Hidden capability:
- Likely KPI:
- Buyer/user/partner:
- Candidate direct evidence:
- Candidate transferable evidence:
- Missing proof:

Original requirement 1:
- Hard gate / preference / boilerplate:
- Evidence needed in resume:
- Interview proof needed:

Role economics:
- Product/deployment:
- Lead source:
- Sales cycle:
- PoC/tender/acceptance:
- Quota/usage/renewal/collection:
- Fixed/variable compensation:

Decision:
- Direct / transition / bridge / watch:
- Apply version:
- Top three resume changes:
- Top three interview stories:
- Portfolio artifact:
```

## 8. Training and evidence backlog

### Priority A — Required for Zhipu commercial interviews
1. MaaS/API commercial vocabulary: model selection, token pricing, context, latency, concurrency, SLA, fine-tuning, RAG/knowledge base and Agent/tool use.
2. AI scenario discovery: problem, users, workflow, data, baseline, success metric, risk and adoption.
3. PoC design: scope, dataset, benchmark, acceptance criteria, timeline and owner.
4. Deployment modes: public API, dedicated instance, private/on-premises and sovereign deployment at a non-engineering level.
5. Model/Agent evaluation: task set, output quality, hallucination/bad cases, tool success and human review.

### Priority B — Malaysia route
1. Malaysia AI market/account map.
2. Government/GLC/enterprise/SI/cloud/data-center ecosystem.
3. Data-residency, privacy and sovereign-AI concepts.
4. English discovery call and solution-pitch rehearsal.
5. Local competitor and substitute map.

### Priority C — Resume/interview proof
1. Confirm MG/FF chronology and conflicting metrics in the career database.
2. Convert India market entry into a complete STAR/CARE story.
3. Convert premium-price Bangladesh win into a value-selling case.
4. Convert Top-150 database into an AI-assisted customer-intelligence case.
5. Document one failure, wrong judgment or lost deal and the resulting process improvement.

## 9. Personal website decision

### Recommendation
Build a **bilingual evidence hub**, not a decorative personal homepage.

### Minimum useful structure
1. Home: one positioning statement and target routes.
2. Case study — 0→1 India market entry.
3. Case study — premium-price account conversion.
4. Case study — Top-150 customer-intelligence workflow.
5. AI artifact — customer-intelligence Agent with architecture, sample output, evaluation and bad cases.
6. Zhipu/Malaysia artifact — a short market-entry and sovereign-AI opportunity brief.
7. AI solution artifact — mock enterprise discovery and PoC plan using BigModel capabilities.
8. About/contact: keep private details controlled; public repository remains anonymized.

### Website quality gate
The site is valuable only if it proves at least one of:
- better research;
- better AI workflow design;
- better product/solution thinking;
- better English communication;
- clearer business outcomes.

A generic biography, skills list or AI-generated visual site adds little hiring value.

## 10. Questions for candidate evidence discovery

1. Have you sold or supported projects in Malaysia, Singapore or Southeast Asia beyond the currently recorded regions?
2. Are you willing to relocate to Malaysia, and what travel/relocation limits apply?
3. Have you worked with government, state-owned, airport, education or enterprise procurement processes? What documents and stages did you own?
4. Have you ever defined a pilot, sample test, acceptance criterion or technical success metric with a customer?
5. Have you explained an API, software, cloud service, subscription or usage-based price to a customer?
6. Have you coordinated engineers in a live customer demo or technical objection meeting?
7. Do you have examples of data security, privacy, customs/compliance or local certification concerns changing a deal?
8. What forecasting, CRM pipeline, quota and collection responsibilities did you personally own?
9. Can you deliver a ten-minute English product/solution presentation and discovery conversation?
10. Which AI tools or APIs have you personally used, what workflow did you build and how did you evaluate output quality?

## 11. Retrieval-policy repair for future searches

- Start every target-company run with the official career portal and record the ATS type.
- Run both title queries and responsibility-cluster queries.
- Search all active locations, including international roles, before user-constraint ranking.
- Store user-supplied links immediately, even when extraction fails.
- For SPA/hash pages, never treat an unindexed role as nonexistent.
- For BOSS/mobile pages, capture title, JD text, salary, city, recruiter and checked date during the same session.
- Report `JD_TEXT_PENDING` rather than producing a confident fit analysis from the title alone.

## 12. Source notes

- Moka API documentation: https://www.mokahr.com/docs/api/index.html
- BigModel official platform: https://bigmodel.cn/
- BigModel official documentation: https://docs.bigmodel.cn/cn/guide/start/introduction
- BigModel enterprise service: https://www.bigmodel.cn/enterprise-service
- Exact six JD links: recorded in Section 2.

## 13. Change log

### 2026-06-28 — v0.1
- Created the fixed job-requirements database.
- Captured six user-supplied Zhipu links with stable IDs.
- Recorded the technical and policy reasons the earlier search missed them.
- Added a preliminary Malaysia overseas-sales capability model without pretending the inaccessible JD text was verified.
- Mapped existing candidate evidence, gaps, training needs and website requirements.
- Exact per-JD analysis remains blocked until the page text or screenshots are captured.
