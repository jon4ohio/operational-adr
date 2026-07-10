# Extraction — Portfolio ADR-008

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/ADR-008-adr-update-gate-for-major-pushes.md`  
**Date extracted:** 2026-07-09

## What happened?

Established mandatory ADR checkpoint for major pushes: create, supersede, or document "no ADR needed" before push completion.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Architecture-affecting pushes documented only when remembered → code/rationale drift | recording threshold |
| What evidence existed? | Observed drift risk from larger pushes (theme, tokens, routing) | evidence source |
| What alternatives were rejected? | Option B (optional/informal ADR updates) rejected for traceability | rejected alternatives preserved |
| How was confidence expressed? | Accepted; risks table; Review Schedule 2026-07-10 | confidence expression |
| How could this be superseded? | "Create new ADR to relax scope without altering this accepted ADR" | supersession trigger |
| What governance rule is implicit? | Meta-governance: defines WHEN ADRs are required | recording threshold |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Drift observation | Context (narrative) | Yes |
| Enforcement | CONTRIBUTING + README references | No |
| Index discipline | docs/adrs/index.md required update | No |

## Primitive chain

```text
ADR-008
  → Recording threshold: major push = architecture/tokens/routing/data model/workflow
  → Meta-governance ADR: governs ADR creation itself
  → Alternatives: mandatory checkpoint vs optional judgment
  → Enforcement via contributor docs + checklist
  → Index update required when new ADRs added
  → Supersession: new ADR to relax policy (immutability preserved)
```

## Notes

Strongest recording-threshold primitive in portfolio corpus. Self-referential governance.
