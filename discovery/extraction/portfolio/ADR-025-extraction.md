# Extraction — Portfolio ADR-025

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/ADR-025-orchestrated-portfolio-case-study-card-copy.md`  
**Date extracted:** 2026-07-09

## What happened?

Chose short title + subtitle for orchestrated-portfolio card. Later superseded by ADR-026.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Long provocative title poor for card scanability | recording threshold |
| What evidence existed? | Card pattern on other projects; positioning vocabulary needs | evidence source |
| What alternatives were rejected? | Option A (keep long title) vs Option B (short + subtitle) | rejected alternatives preserved |
| How was confidence expressed? | Initially Accepted; Status later "Superseded by ADR-026" | confidence expression |
| How could this be superseded? | ADR-026 superseded this record | supersession trigger |
| What governance rule is implicit? | Related ADRs constrain; supersession chain maintained in index | supersession trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| UI pattern | Context (work index cards) | Yes |
| Supersession | Status line + Related ADRs | Yes |

## Primitive chain

```text
ADR-025
  → Recording threshold: copy/positioning affects listing UX
  → Decision made and later superseded (not amended in place)
  → Status: Superseded by ADR-026
  → Related ADRs link forward to superseding record
```

## Notes

Illustrates immutability + supersession chain. Decision partially reversed by narrative refresh in ADR-026.
