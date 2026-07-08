# July 2026 Workflow Improvements

This file tracks proposed improvements to the daily loop and company-research workflow.

## Improvement table

| Improvement | Trigger | Status | Next action |
|---|---|---|---|
| GitHub-grounded daily loop | User requested daily task to read GitHub first, then search and write back compressed updates | testing | Keep visible GitHub Preflight Checklist as first output in every serious automation run |
| Mandatory GitHub preflight gate | Automation previously began external search without proving repository context was loaded | testing | If any future comparable run lacks `GitHub Preflight Checklist`, record evolution trigger and repair automation/runtime path |
| July working cache | User requested a monthly cache for active work memory | testing | Continue updating only compressed decision-changing deltas |
| Dashboard view | User requested a current view of directions, companies, roles and improvements | testing | Use `docs/JOB_SEARCH_DASHBOARD.md` and July dashboard cache |
| HTML delivery | Automation runtime failed to create a downloadable HTML file in this run | blocked / runtime issue | Continue chat report; retry HTML only when file-write tooling is available; do not claim success without a real link |

## Rules

- Do not turn one-off preferences into global policy.
- Repeated workflow failures should become evolution triggers.
- Accepted improvements should be summarized in `memory/RUN_SUMMARY.md`.
- Protected-policy changes require a dedicated patch and replay checks.
