# Evolution Run Template

## Self-model snapshot

- Trigger:
- Active policy/ref (`π_job`):
- Evolution procedure/ref (`I_job`):
- Frozen evaluator/ref (`U_job`):
- Deployment evidence (`r_job`):
- Protected goals (`g_job`):
- Rollback policy/ref:
- Editable files:
- Frozen files:
- Complexity budget:

## Failure model

- Observed failure:
- Reproduction case:
- Why current policy causes it:
- Non-target routes at risk:

## Candidate patches

### Candidate A

- Hypothesis:
- Exact change:
- Expected trace:
- Risk:
- Lifecycle:
- Rollback:

### Candidate B

- Hypothesis:
- Exact change:
- Expected trace:
- Risk:
- Lifecycle:
- Rollback:

## Replay matrix

| Case | Baseline | Candidate | Evaluator result | Regression? |
|---|---|---|---|---|
| Target failure | | | | |
| Contrast route | | | | |
| Fresh unseen case | | | | |

## Decision

- Accepted candidate:
- Evidence:
- Rejected alternatives:
- Protected invariants preserved:
- Complexity delta:
- Monitoring window:
- Automatic rollback condition:

## PR checklist

- [ ] One compact patch only.
- [ ] Evaluator/constitution unchanged.
- [ ] Target, contrast and fresh cases run.
- [ ] Writeback and source traceability pass.
- [ ] Active and rollback refs recorded.
- [ ] Company-specific exceptions remain in ledger.
