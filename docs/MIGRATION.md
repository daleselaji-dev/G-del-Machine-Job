# Canonical Memory Migration

## Decision

GitHub becomes the canonical store for policy, state, evaluation, field map and evolution history. Google Drive is no longer a required runtime dependency.

## Migrated concepts

- current 60-day interview objective and funnel state;
- compact runtime policy;
- stable preferences and one-row-per-company ledger;
- latest run summaries and unresolved triggers;
- company-outlook evidence gate;
- Chinese-company 职Q-first employer research;
- HTML/mobile output contract;
- bounded Gödel evolution, frozen evaluator and rollback;
- Field Onboarding Map for open career directions and capability transitions.

## Deliberately not migrated

- raw conversation history;
- duplicate company rows;
- every reviewed job and source snippet;
- personal contact details;
- unsupported company or employee claims;
- obsolete prompt versions that no longer change behavior.

## Runtime cutover

After the bootstrap PR is merged:

1. automation and manual runs load the repository files first;
2. writeback is performed through a branch/commit or approved direct state update;
3. policy/evaluator changes use a dedicated PR;
4. Drive files remain historical backup only and must not silently override GitHub state;
5. a GitHub read failure returns `MEMORY_READ_FAILED` rather than falling back to stale chat memory.

## Validation

The cutover is complete only after the frozen evaluator passes:

- direct-fit job search;
- large-model transition search;
- cross-direction contrast search;
- company-ledger update without policy leakage;
- writeback/readback recovery test.
