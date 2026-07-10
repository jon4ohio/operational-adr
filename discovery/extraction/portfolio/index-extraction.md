# Extraction — Portfolio docs/adrs/index.md

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/index.md`  
**Date extracted:** 2026-07-09

## What happened?

Canonical table of 82+ ADRs with Status and Superseded By column. Companion to individual ADR files.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Ongoing index maintenance discipline (ADR-008 requires updates) | recording threshold |
| What evidence existed? | Not a decision record — governance infrastructure | evidence source |
| What alternatives were rejected? | N/A | — |
| How was confidence expressed? | Status per row; Superseded By column | confidence expression |
| How could this be superseded? | Index rows updated when ADRs superseded; not replaced wholesale | supersession trigger |
| What governance rule is implicit? | Single lookup for validity and supersession chain | supersession trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Decision status | Index table | Yes |
| Supersession chain | Superseded By column | Yes |
| Full rationale | Individual ADR-NNN files | No |

## Primitive chain

```text
index.md
  → Governance infrastructure separate from individual ADRs
  → Supersession chain machine-readable at index level
  → Required update on new ADR (per ADR-008)
  → 82+ decisions navigable without reading all files
```

## Notes

Index enables "is this decision still valid?" without opening each ADR. No direct Anchor equivalent at same scale.
