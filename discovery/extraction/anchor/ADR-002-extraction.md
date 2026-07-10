# Extraction — Anchor ADR-002

**Corpus:** Anchor meta-repo  
**Artifact:** `docs/decisions/ADR-002-framework-vs-experience.md`  
**Date extracted:** 2026-07-09

## What happened?

Anchor split Framework (seven contracts) from Experience (adoption docs), renamed bootstrap terminology, and established parallel governance rules for framework vs Experience evolution.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Recurring architectural tension: adoption teaching vs framework contracts; language mismatch ("bootstrap") | recording threshold |
| What evidence existed? | ADR-001 freeze context; adoption-as-product tension from refinement work | evidence source |
| What alternatives were rejected? | Options A–C with description, pros, cons, effort, notes | rejected alternatives preserved |
| How was confidence expressed? | Accepted; Decision Drivers; risks table; Review Schedule with date and owner | confidence expression |
| How could this be superseded? | "Supersede with ADR documenting reversion if two-product split fails validation" | supersession trigger |
| What governance rule is implicit? | Framework changes need two independent projects; Experience expands after repeated adoption questions | recording threshold, review trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Prior decision | ADR-001 referenced in Context | No (link) |
| Adoption friction | Implied in Context; not tabulated | No |
| Governance rules | Decision body + Operational Impact | Yes |

## Primitive chain

```text
ADR-002
  → Recording threshold: recurring tension between product layers
  → Evidence source: prior ADR + refinement observations (narrative)
  → Scope boundary: explicit In scope / Out of scope
  → Alternatives preserved: three options, one marked chosen
  → Confidence expression: Drivers + risks + scheduled review
  → Supersession trigger: conditional supersede on validation failure
  → Decision ownership: Project maintainer
```

## Notes

First Anchor ADR with full governance metadata pattern (drivers, review schedule, structured options).
