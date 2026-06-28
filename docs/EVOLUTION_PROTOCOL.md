# Bounded Gödel Evolution Protocol

## Purpose

Allow the career agent to improve from repeated use and feedback without prompt bloat, self-approval, evaluator drift or irreversible regressions.

## Control separation

- `π_job`: active runtime policy in `SKILL.md`.
- `I_job`: this evolution procedure.
- `U_job`: frozen evaluator in `evals/EVALUATION_TASKS.md`.
- `r_job`: deployment evidence in reports, interview outcomes, user feedback and `memory/RUN_SUMMARY.md`.
- `g_job`: protected goals in `docs/CONSTITUTION.md`.

## Ordinary run boundary

An ordinary run may:

- execute the active policy;
- update state, company ledger and compressed run summary;
- record an `Evolution Trigger`.

It may not:

- edit `SKILL.md` or this protocol;
- alter the evaluator or constitution;
- create a new global rule for one company or one anecdote;
- merge a patch or change the active/rollback version.

## Trigger conditions

Start an evolution review only when at least one condition holds:

1. durable user feedback changes ranking, evidence, route or delivery;
2. the same failure occurs in two or more completed comparable runs;
3. the frozen evaluator returns the same repair twice;
4. a recommended role/company later violates a protected constraint;
5. memory, HTML, evidence traceability or writeback fails;
6. the current policy produces unnecessary complexity or repeated memory duplication.

A single preference about one company normally updates the ledger, not the policy.

## Evolution cycle

### Step 1 — Self-model snapshot

Record:

- active policy commit/ref;
- rollback policy commit/ref;
- editable files;
- frozen files/evaluator;
- protected goals;
- triggering evidence;
- expected target improvement;
- possible non-target regressions;
- resource/change budget.

### Step 2 — Candidate generation

Generate 1–3 surgical patches.

Each candidate states:

- failure mode;
- hypothesis;
- exact file/section change;
- expected behavioral trace;
- risk and non-target route affected;
- rollback method;
- lifecycle: permanent, provisional or experiment.

Prefer replacing, compressing or clarifying existing rules. Reject patches that merely add another checklist or company exception.

### Step 3 — Evaluator firewall

Freeze `U_job` and `g_job` before testing.

A candidate fails closed if it:

- changes target behavior and its evaluator in the same cycle;
- weakens hard constraints or evidence requirements to pass;
- removes rollback or traceability;
- relies on hidden author context not present in the repository.

Evaluator changes require a separate evaluator-evolution cycle while `π_job` is frozen.

### Step 4 — Replays

Run baseline and candidate using the same evidence pool and tool conditions.

Minimum cases:

1. **Target case** — reproduces the trigger/failure.
2. **Contrast case** — a different route that must not regress.
3. **Fresh case** — previously unused case to detect overfit.

For global changes, include at least one company-research case and one memory/output case.

### Step 5 — Acceptance

Accept only if:

- the target failure improves materially;
- no protected invariant is broken;
- no meaningful contrast/fresh-case regression appears;
- evidence traceability and writeback still work;
- the patch remains within the agreed complexity budget;
- rollback is executable.

At most one compact patch is accepted per cycle.

### Step 6 — PR and deployment

- create a dedicated branch;
- update only the required files;
- include an evolution record and replay results in the PR body;
- request review when available;
- merge only after acceptance;
- update `memory/ROLLBACK.md` and the active version in `memory/STATE.md`;
- monitor the next three comparable runs.

## Rollback conditions

Rollback immediately when:

- a protected constraint is violated;
- factual/evidence quality degrades;
- company-specific exceptions leak into global policy;
- memory size grows without decision value;
- three comparable production runs score below the rollback policy;
- a writeback failure makes state unreliable.

## Meta-improver rule

A successful patch proves only that a candidate `π_job` performed better on the evaluated cases.

Do not claim that `I_job` improved unless the old and candidate evolution procedures are compared on multiple new, previously unseen failure cases under the same frozen evaluator and resource budget.

## Evolution record template

```text
Evolution Run
- Trigger:
- Starting policy/ref:
- Rollback policy/ref:
- Frozen evaluator/ref:
- Protected goals:
- Candidate patch:
- Target replay:
- Contrast replay:
- Fresh replay:
- Resource/complexity delta:
- Decision: accept / reject / repair
- Rollback condition:
- Monitoring window:
```
