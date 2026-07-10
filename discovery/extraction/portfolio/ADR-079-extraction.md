# Extraction — Portfolio ADR-079

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/ADR-079-retire-leadership-route-essay-relocation.md`  
**Date extracted:** 2026-07-09

## What happened?

Deleted /leadership route; surfaced essay as forthcoming homepage Writing entry. Triggered by ADR-008 major-push gate.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | IA change (route table, nav, search, graph); qualifies under ADR-008 gate | recording threshold |
| What evidence existed? | Page became "article disguised as page"; homepage Writing already handles discovery | evidence source |
| What alternatives were rejected? | Options A (keep route), B (delete + forthcoming), C (301 redirect) | rejected alternatives preserved |
| How was confidence expressed? | Accepted; risks table; Review Schedule tied to essay publication or 2027-07-07 | confidence expression |
| How could this be superseded? | Restore page from git; revert nav/footer/search/graph changes | supersession trigger |
| What governance rule is implicit? | ADR-008 dependency; stale rationale in ADR-055 noted; supersedes ADR-041 in effect | recording threshold, supersession trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| ADR gate | ADR-008 cited in Context and Related ADRs | No (link) |
| Stale prior rationale | ADR-055 constraint noted as stale | No (link) |
| Implementation files | References section (6+ file links) | No |

## Primitive chain

```text
ADR-079
  → Recording threshold: public IA change triggers ADR-008
  → Depends on meta-governance ADR-008
  → Supersedes ADR-041 in effect (page deleted)
  → Amends ADR-075 URL-stability note
  → Marks ADR-055 Option A rationale stale
  → Related ADRs use typed relationships (depends on, supersedes, constrains, amends)
```

## Notes

Strongest example of supersession graph and stale-rationale handling in portfolio corpus.
