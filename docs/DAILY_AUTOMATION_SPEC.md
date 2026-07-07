# Daily Automation Spec

Status: reference v1

## Schedule

Daily run, around 09:00-10:00 Asia/Taipei time.

## Purpose

Run a longer, information-complete but modular job-search discovery process that supports the user's long-term career planning.

## Run scope

Each daily run should cover:

1. updated direction map;
2. 3-5 active or emerging subsectors;
3. 6-7 L0 company candidate cards;
4. 2-3 L1 quick screens;
5. at most 1 L2 deep-dive candidate;
6. role pipeline update;
7. interview queue update;
8. evidence gaps;
9. workflow improvement notes;
10. durable memory suggestions.

## Discovery entrances

### Entrance A — industry first

Start from AI-connected, future-facing subsectors. Find head companies, hidden champions and foreign-company YRD teams. Then search for matching roles.

### Entrance B — company first

Start from strong Yangtze River Delta companies. Check product, customer, industry value and role fit.

## Output standard

Use `templates/daily_job_discovery_update.md`.

Keep output comprehensive but modular:

- dashboard first;
- details by module;
- evidence labels;
- next actions;
- no unsupported recommendation.

## Memory rule

Only preserve decision-changing information:

- current campaign state to `memory/STATE.md`;
- stable preference or company state to `memory/PREFERENCES_AND_COMPANY_LEDGER.md`;
- compressed run summary and unresolved triggers to `memory/RUN_SUMMARY.md`;
- confirmed candidate evidence or interview feedback to `profile/EXPERIENCE_APPEND_ONLY.md`.

Do not store raw daily search results, every reviewed company, every anonymous review or temporary hypotheses as durable memory.

## Quality check

Before completion, verify:

- no more than one L2 company is promoted unless explicitly requested;
- role freshness is separated from company attractiveness;
- employer risk is not hidden;
- biggest evidence gaps are listed;
- next three actions are concrete.
