# Architecture

## Control objects

The project separates five control objects:

- `π_job` — executable job-search policy (`SKILL.md`).
- `I_job` — evolution procedure (`docs/EVOLUTION_PROTOCOL.md`).
- `U_job` — frozen evaluator (`evals/EVALUATION_TASKS.md` and reviewer gates).
- `r_job` — deployment evidence (`memory/RUN_SUMMARY.md`, reports, user/recruiter feedback).
- `g_job` — protected goal and invariants (`docs/CONSTITUTION.md`).

A candidate patch may change `π_job` or, in a separate cycle, `I_job`; it may not change the target behavior and its own acceptance gate in the same cycle.

## System map

```mermaid
flowchart TD
    U[User goals, feedback, interview events] --> O[Orchestrator]
    O --> M[Load canonical GitHub memory]
    M --> R{Run mode}

    R -->|Ordinary run| D[Discover current roles]
    D --> F[Field Onboarding Map]
    F --> C[Company / product / role due diligence]
    C --> S[Rank P0/P1/P2/WATCH/REJECT]
    S --> H[Mobile briefing + HTML report]
    H --> W[Compressed writeback]
    W --> E[Deployment evidence r_job]

    E --> T{Evolution trigger?}
    T -->|No| X[End / next scheduled run]
    T -->|Yes| Q[Record trigger only]

    R -->|Evolution cycle| SM[Self-model snapshot]
    SM --> P[Generate 1-3 surgical patches]
    P --> B[Baseline vs candidate on same evidence]
    B --> V[Frozen evaluator U_job]
    V --> G{Protected goals g_job preserved?}
    G -->|No| RB[Reject / rollback]
    G -->|Yes| A{Target improves and contrast/fresh cases pass?}
    A -->|No| RB
    A -->|Yes| PR[Pull request with rollback point]
    PR --> MR[Review and merge]
    MR --> X
```

## Memory architecture

```mermaid
flowchart LR
    C[CONSTITUTION\nprotected invariants] --> SK[SKILL\nactive policy]
    FM[FIELD ONBOARDING MAP\ncareer-space model] --> SK
    EV[EVIDENCE & DD\nresearch rules] --> SK
    SK --> ST[STATE\ncurrent goal/funnel/version]
    SK --> CL[COMPANY LEDGER\none current row per company]
    SK --> RS[RUN SUMMARY\nlatest 5 + triggers]
    RS --> EP[EVOLUTION PROTOCOL]
    EP --> PR[Branch / PR]
    PR --> SK
    PR --> RB[ROLLBACK]
```

## Agent roles

The roles are logical responsibilities, not mandatory separate processes.

| Role | Job |
|---|---|
| Orchestrator | Select run mode, route mix, workload and stop conditions. |
| Source Scout | Find current openings and high-quality company/product sources. |
| Role Analyst | Map JD to actual product, customer, economics and daily work. |
| Company Analyst | Evaluate outlook, product position, commercial quality and employer risk. |
| Field Map Builder | Maintain directions, transitions, capability gaps and bridge roles. |
| Application Strategist | Choose resume version, contact path and interview narrative. |
| Reviewer | Apply frozen evidence, ranking, output and regression gates. |
| Memory Steward | Compress updates and prevent prompt/document bloat. |
| Evolution Steward | Run isolated candidate patches, tests and rollback. |

## Data lifecycle

```mermaid
stateDiagram-v2
    [*] --> Discovered
    Discovered --> Verified: current role and source confirmed
    Discovered --> Dropped: expired / vague / obvious mismatch
    Verified --> Researched: product + company + employer evidence
    Researched --> Ranked
    Ranked --> Applied: user confirms application
    Ranked --> Watch
    Ranked --> Rejected
    Applied --> Screening
    Screening --> FirstRound
    FirstRound --> SecondRound
    SecondRound --> Offer
    Applied --> Closed: rejection / withdrawal / role closed
    Screening --> Closed
    FirstRound --> Closed
    SecondRound --> Closed
```

## Change boundaries

- Runtime evidence can change state, ledger and run summary.
- Company-specific findings never enter the global skill.
- Stable user preferences enter the ledger only after they affect future decisions.
- Global policy changes require an evolution PR.
- Evaluator changes require a separate evaluator-evolution PR with the target policy frozen.
