# Startup Load Reference Notes

Date: 2026-07-07
Status: companion note for PR #7

A startup-load evolution record already exists in this PR. The key implementation decision is to keep workflow reference files separate from active policy until a dedicated startup-load patch connects them.

Preferred follow-up:

- base branch: `evolution/workflow-system-v1`
- head branch: `evolution/startup-load-reference-v1`
- change: update `SKILL.md` load order to reference `docs/RUN_LOAD_REFERENCE.md`
- review focus: normal job-search tasks must not become over-heavy
