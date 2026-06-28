# Candidate Profile Archive

This directory stores the candidate's reusable experience evidence for role matching, resume generation and interview preparation.

## Design

- `BASELINE_RESUME.md` — immutable, anonymized baseline extracted from the current resume.
- `EXPERIENCE_APPEND_ONLY.md` — new facts, projects, achievements, interview feedback and corrections. Append only.
- `SEARCH_INDEX.md` — searchable capability and evidence index. It may be regenerated, but source entries are never deleted.
- `SOURCE_REGISTRY.md` — source provenance and import notes.

## Append-only rule

1. Do not delete or rewrite factual source entries in `BASELINE_RESUME.md` or `EXPERIENCE_APPEND_ONLY.md`.
2. Add new information with a unique evidence ID and date.
3. When a fact is corrected, append a `SUPERSEDES:` entry rather than erasing the old record.
4. Resume versions may select and rewrite evidence for a target role, but they do not replace the archive.
5. Sensitive personal identifiers are excluded because the repository is public.

## Retrieval rule

Before evaluating a role, search `SEARCH_INDEX.md` for the job's responsibilities, industry, customers, tools and capability requirements. Open the referenced evidence IDs, then map only supported evidence to the role.
