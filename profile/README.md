# Candidate Profile Archive

This directory stores the candidate's reusable experience evidence and target-role requirements for role matching, resume generation and interview preparation.

## Design

- `CAREER_EVIDENCE_DATABASE.md` — fixed working database for resume evidence, story angles, preferred wording, conflicts and expansion prompts.
- `JOB_REQUIREMENTS_DATABASE.md` — fixed working database for target JDs, hidden capability demands, candidate-fit mapping, training gaps and portfolio actions.
- `BASELINE_RESUME.md` — immutable, anonymized baseline extracted from the current resume.
- `EXPERIENCE_APPEND_ONLY.md` — source log for new facts, projects, achievements, interview feedback and corrections. Append only.
- `SEARCH_INDEX.md` — searchable capability and evidence index. It may be regenerated, but source entries are never deleted.
- `SOURCE_REGISTRY.md` — source provenance and import notes.

## Append-only rule

1. Do not delete or rewrite factual source entries in `BASELINE_RESUME.md` or `EXPERIENCE_APPEND_ONLY.md`.
2. Add new information with a unique evidence ID and date.
3. When a fact is corrected, append a `SUPERSEDES:` entry rather than erasing the old record.
4. Maintain `CAREER_EVIDENCE_DATABASE.md` as the concise resume-facing view: spelling fixes may happen in place; factual changes retain history; useful alternate wording may remain.
5. Maintain `JOB_REQUIREMENTS_DATABASE.md` as the requirement-facing view: preserve exact JD wording, separate facts from inference and record why a role was discovered or missed.
6. Resume versions select and rewrite supported evidence for a target role, but they do not replace either database or the source archive.
7. Sensitive personal identifiers are excluded because the repository is public.

## Retrieval rule

For a target role, start with `JOB_REQUIREMENTS_DATABASE.md` to identify the actual capability and proof requirements, then retrieve matching evidence from `CAREER_EVIDENCE_DATABASE.md`. Use `SEARCH_INDEX.md` for broader responsibility/industry/tool retrieval, and open the referenced baseline or append-only evidence before asserting a disputed or high-impact fact.