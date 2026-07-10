# Extraction — Portfolio docs/adrs/LOG.md

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/LOG.md`  
**Date extracted:** 2026-07-09

## What happened?

Chronological audit log of ADR acceptance events, index audits, supersession notes, and implementation notes. Companion to index.md.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Audit trail for bulk ADR activity and index verification | recording threshold |
| What evidence existed? | Dated events with ADR numbers and supersession notes | evidence source |
| What alternatives were rejected? | N/A | — |
| How was confidence expressed? | Dated entries; Proposed → Accepted transitions logged | confidence expression |
| How could this be superseded? | Append-only chronology; corrections via new entries | supersession trigger |
| What governance rule is implicit? | Index integrity verified periodically; supersession logged at acceptance time | review trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Acceptance events | LOG table rows | Yes |
| Index audits | LOG entries (e.g. 2026-04-13 merge check) | Yes |
| ADR content | Individual files | No |

## Primitive chain

```text
LOG.md
  → Chronological governance audit (not decision rationale)
  → Logs supersession at acceptance ("Supersedes: ADR-025")
  → Index audit entries (row count vs file count)
  → Implementation notes appended to ADR decisions post-acceptance
```

## Notes

Third governance artifact alongside ADR files and index. Anchor has Handoff friction log but not ADR-specific chronology.
