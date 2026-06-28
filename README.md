# G-del Machine Job

A bounded self-evolving career-search agent that combines **Gödel-style policy evolution** with a **Field Onboarding Map** for job discovery, company/product due diligence, application strategy, interview conversion, and durable memory.

## Canonical source

This GitHub repository is the single source of truth. Google Drive is treated only as migration history and is no longer authoritative.

## What the system optimizes

- Reach qualified interviews within the active search window.
- Prioritize companies with credible industry and product prospects.
- Keep overseas sales, multinational commercial roles, enterprise AI/data/cloud, robotics, industrial technology, and adjacent bridge roles open.
- Convert user feedback into small, tested policy improvements rather than an ever-growing prompt.
- Preserve evidence, rollback, and evaluator independence.

## Start here

1. [`PROJECT.md`](PROJECT.md) — current project state and operating goal.
2. [`SKILL.md`](SKILL.md) — executable agent skill.
3. [`docs/ARCHITECTURE.md`](docs/ARCHITECTURE.md) — system map and components.
4. [`docs/CONSTITUTION.md`](docs/CONSTITUTION.md) — protected invariants.
5. [`docs/EVOLUTION_PROTOCOL.md`](docs/EVOLUTION_PROTOCOL.md) — bounded Gödel evolution.
6. [`memory/STATE.md`](memory/STATE.md) — current state and interview funnel.
7. [`memory/PREFERENCES_AND_COMPANY_LEDGER.md`](memory/PREFERENCES_AND_COMPANY_LEDGER.md) — stable preferences and company states.

## Repository rule

Ordinary daily runs may update runtime memory, but **must not edit the policy, evaluator, or constitution**. Policy changes happen only through a dedicated evolution branch or pull request with baseline/candidate evaluation and rollback.
