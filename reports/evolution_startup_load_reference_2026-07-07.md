# Evolution Record — Startup Load Reference

Date: 2026-07-07
Related PR: #7
Status: proposed follow-up

## Trigger

User requested that the Goal agent / bounded evolution rules be included in the content read at the beginning of future workflow-design and company-research tasks.

## Starting policy/ref

Current active policy reads `docs/CONSTITUTION.md`, state, preferences/company ledger, profile search index, evidence/DD rules, field onboarding map and evaluator.

## Protected goals

The change must preserve:

- truthfulness;
- career quality;
- evidence traceability;
- user constraints;
- open career field;
- bounded evolution and evaluator independence.

## Candidate patch

Two possible implementation paths:

1. Minimal path: add `docs/EVOLUTION_PROTOCOL.md` to the existing startup load order in `SKILL.md`.
2. Manifest path: add `docs/RUN_LOAD_REFERENCE.md` as a startup reference, then task-specific workflow files are loaded only when relevant.

## Target replay

Company DD workflow-design case passed. The new workflow reduced information overload by separating L0, L1 and L2 stages.

## Contrast replay

Normal job-search task passed with caution. The workflow should not force L2 due diligence for every company.

## Fresh replay

Fresh SEER Robotics L0/L1 case passed. The workflow promoted a promising company to L1 without unsupported recommendation.

## Risk

The manifest path may add extra reading burden if loaded for every casual task. Therefore it should be task-specific, not universal for all chat.

## Recommendation

Use the manifest path as a reference now. After PR #7 is accepted, a small active-policy patch may connect `docs/RUN_LOAD_REFERENCE.md` from `SKILL.md`.

## Rollback condition

Rollback if the startup reference causes normal job-search tasks to become slower, more verbose or over-researched without improving decision quality.
