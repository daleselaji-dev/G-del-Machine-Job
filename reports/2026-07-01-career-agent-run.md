# G-del Career Agent Run — 2026-07-01

## Load result

Required files were read from `main`:

1. `docs/CONSTITUTION.md`
2. `memory/STATE.md`
3. `memory/PREFERENCES_AND_COMPANY_LEDGER.md`
4. `profile/SEARCH_INDEX.md`
5. `SKILL.md`
6. `docs/EVIDENCE_AND_DD.md`
7. `docs/FIELD_ONBOARDING_MAP.md`
8. `evals/EVALUATION_TASKS.md`

`MEMORY_READ_FAILED`: false.

## Profile-first retrieval

Before ranking companies, the run used `profile/SEARCH_INDEX.md` and opened relevant evidence in `profile/BASELINE_RESUME.md` and `profile/EXPERIENCE_APPEND_ONLY.md`.

Relevant supported role families:

- 海外运营 / International Operations
- 产品运营 / Product Operations
- 客户成功 / Customer Success
- 生态运营 / Ecosystem Operations
- 技术解决方案销售
- AI / MaaS商业化
- AI产品运营 / Agent数据
- 海外销售 / International Sales

## Current-source scan

### DeepSeek

- Ranking: `P1-WATCH`
- Current evidence: official site has a recruiting entry through Mokahr; Reuters and FT reported fresh expansion/hiring around 2026-06-25/26.
- Limitation: the Mokahr page could not be parsed in this run, so no exact JD/title/salary/location is treated as verified.
- Candidate evidence:
  - Direct/near evidence: EXP-FF-001-D data review and strategy iteration; EXP-MG-001-D customer segmentation, enablement and adoption; EXP-BENY-001-B GTM content.
  - Transferable evidence: EXP-FF-001-F product feedback loop; APP-20260628-01 AI Agent learning.
  - Missing proof: public Agent project, evaluation set, PRD, user-flow and badcase-analysis artifact.
- Action: prepare a DeepSeek-facing one-page portfolio around customer-intelligence Agent, industry lead scoring and feedback-loop operations.

### Unitree / 宇树科技

- Ranking: `P1/P2 bridge`
- Current evidence: official site confirms product lines across consumer/education robots, industry robots, humanoid robots, robotic arms, perception and industrial applications; it also exposes sales/HR/contact and industry purchase paths.
- Limitation: no current official job-list page was parsed in this run, so role title and salary are not verified.
- Candidate evidence:
  - Direct/near evidence: EXP-FF-001-B technical-product ramp; EXP-MG-001-C overseas customer development; EXP-MG-001-E project coordination; EXP-FF-001-F product feedback and localized sell-out.
  - Transferable evidence: technical solution sales, overseas operations, customer training and partner enablement.
  - Missing proof: robotics-specific vocabulary, on-site deployment/technical support evidence and target-team employer evidence.
- Action: prepare a robotics solution-sales / overseas-commercial bridge resume version without claiming direct robotics experience.

### Z.ai / 智谱

- Ranking: `WATCH`
- Current evidence: Reuters reported 2026-06-25 momentum around Z.ai/GLM and listing plans; product direction remains relevant to MaaS, Agent and commercialization.
- Limitation: no current Hangzhou JD was verified in this run.
- Candidate evidence:
  - Transferable evidence: solution/value translation, overseas BD, partner operations, bilingual GTM, customer intelligence.
  - Missing proof: current target JD, salary, team scope and Agent/MaaS portfolio.
- Action: keep on watchlist until current official or recruiting-platform JD is found.

## Interview Queue

1. Build one DeepSeek-facing artifact: customer-intelligence Agent / industry lead scoring / sales-feedback loop.
2. Build one Unitree-facing resume version: 3D-printing technical sales to robotics solution/overseas scenario sales.
3. Manually verify DeepSeek Mokahr and Unitree current roles before applying.

## Delivery status

- Mobile briefing: completed.
- HTML report: `HTML_FAILED` because the local file-generation environment rejected write access.
- Writeback: branch and PR attempted separately.

## Open risks

- No salary, overtime, legal-employment entity, team attainment or employee-review conclusion was verified.
- Chinese employer-risk checks requiring 职Q/看准/脉脉 remain incomplete.
- The Agent/product portfolio gap remains the largest transition blocker.
