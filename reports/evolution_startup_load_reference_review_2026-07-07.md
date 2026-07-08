# Startup Load Reference Review Note

Date: 2026-07-07

## Proposed active-policy follow-up

After PR #7 is reviewed, create a small startup-load patch.

Suggested change:

- add `docs/RUN_LOAD_REFERENCE.md` to the startup/read-order section in `SKILL.md`;
- keep `docs/EVOLUTION_PROTOCOL.md` visible through the reference;
- do not change constitution, evaluator or evidence gates.

## Replay requirement

The patch should reuse the three replays in `reports/workflow_replays_2026-07-07.md`.

## Rollback trigger

Rollback if normal job discovery becomes slower or more verbose without improving decision quality.
