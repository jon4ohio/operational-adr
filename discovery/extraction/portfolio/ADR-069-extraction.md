# Extraction — Portfolio ADR-069

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/ADR-069-evidence-review-experience.md`  
**Date extracted:** 2026-07-09

## What happened?

Added EvidenceImage + EvidenceReviewOverlay for inspectable case study figures without leaving narrative.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Reviewers need fine detail inspection; prior static images only | recording threshold |
| What evidence existed? | Stakeholder need (hiring managers, recruiters); prior behaviour described in Context | evidence source |
| What alternatives were rejected? | Options A (new tab), B (overlay chosen), C (gallery deferred) | rejected alternatives preserved |
| How was confidence expressed? | Accepted; Success criteria enumerated in Decision; risks table | confidence expression |
| How could this be superseded? | Remove EvidenceImage imports; restore plain img (rollback in Operational Impact) | supersession trigger |
| What governance rule is implicit? | Editorial rule embedded in Decision; QA checklist in Operational Impact | scope boundary |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| User need | Context (narrative) | Yes |
| Success criteria | Decision section | Yes |
| Implementation | File references | No (links) |

## Primitive chain

```text
ADR-069
  → Recording threshold: new editorial capability (evidence inspection)
  → Success criteria in Decision (unusual explicitness)
  → Three options with deferral note on Option C
  → Scope boundary: flagship case study figures only
  → Editorial rule: inline readability required without overlay
```

## Notes

"Evidence" in title refers to portfolio screenshots, not governance evidence tables.
