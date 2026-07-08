# Workflow Replay Notes — 2026-07-07

Status: pre-merge check for PR #7

## Purpose

These notes test whether the new workflow controls stage depth, reduces information overload and keeps company research decision-oriented.

## Replay 1 — Target case: company DD workflow design

### Scenario

A user asks for a detailed company background-check workflow after several company-research runs became too comprehensive and hard to act on.

### Expected behavior under new workflow

- Do not produce a single giant checklist as the main output.
- Split research into L0, L1 and L2 stages.
- Present the final user-facing view through six modules:
  1. company development and operating condition;
  2. industry and technology trend;
  3. product competitiveness and sellability;
  4. customers, channels and overseas business;
  5. employer and role quality;
  6. candidate entry ecology.
- Keep detailed evidence available, but compress the dashboard.
- Convert unknowns into meeting-validation questions.

### Result

Pass.

The workflow documents now separate research coverage from presentation and define L0/L1/L2 outputs.

### Remaining risk

The active startup policy has not yet been updated to read the new reference docs automatically.

## Replay 2 — Contrast case: normal job-search task

### Scenario

A user asks for current suitable roles across a direction such as overseas sales, AI commercialization or technical BD.

### Expected behavior under new workflow

- Do not run L2 full DD for every company.
- Use discovery first, then L0 cards for multiple companies.
- Promote only selected companies to L1.
- Keep chat output short and action-oriented.
- Continue to respect existing role gates: current/open role, location, fit, compensation/work-style conflicts and company outlook.

### Result

Pass with caution.

The daily discovery workflow explicitly says most companies should stop at L0 or L1. The risk is that the assistant may still over-research interesting companies unless the active startup policy references these docs.

### Follow-up

After merge, run one normal job-search task and verify that no more than a small subset of companies receives L2 treatment.

## Replay 3 — Fresh L0/L1 case: SEER Robotics / 仙工智能

### Scenario

A fresh company is considered for the Yangtze River Delta technology-company map.

### Public signals used for this replay

- SEER Robotics / 仙工智能 is associated with Shanghai and robot control systems.
- Public search results describe products such as robot controllers, mobile robots, navigation/localization modules and software platforms.
- Public search results also describe international activity and offices/subsidiary signals, but those require source-level verification before any recommendation.

### L0 behavior

The company should not immediately receive a full DD report.

L0 output should capture:

| Field | Value |
|---|---|
| Company | SEER Robotics / 仙工智能 |
| City | Shanghai |
| Subsector | robotics, AMR, robot control systems |
| Product one-liner | robot controllers, mobile robots and software platforms |
| Customer one-liner | industrial manufacturing and logistics automation customers |
| AI/tech adjacency | high, but exact role tie must be verified |
| Initial stage | L0-pass to L1, not direct recommendation |

### L1 behavior

L1 should ask:

- Is there a current YRD role matching overseas sales, channel, BD, solution or product operations?
- Is the role tied to core controller/software products or only generic sales execution?
- Are overseas customers, integrators or partners visible and current?
- Is compensation/work system compatible with user constraints?
- Does the role provide a useful ecology: robotics control systems, integrator ecosystem, industrial customers and possible AI/embodied-intelligence bridge?

### Result

Pass.

The workflow correctly promotes a promising technology company to L1 rather than making an unsupported recommendation.

### Remaining unknowns

- current role status;
- compensation and work system;
- exact product line tied to the role;
- overseas/customer evidence quality;
- team and manager quality.

## Replay summary

| Replay | Result | Note |
|---|---|---|
| Target company-DD workflow | Pass | Modules and stages solve the information-overload problem. |
| Contrast normal job search | Pass with caution | Requires active-policy reference to avoid over-research. |
| Fresh SEER Robotics L0/L1 | Pass | Promotes to L1 but avoids unsupported recommendation. |

## Recommendation

PR #7 is suitable for review as a reference-doc/template patch. A later small patch should connect `docs/RUN_LOAD_REFERENCE.md` to active startup behavior after protected-policy review.
