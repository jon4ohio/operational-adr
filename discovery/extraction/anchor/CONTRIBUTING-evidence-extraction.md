# Extraction — Anchor CONTRIBUTING evidence gates

**Corpus:** Anchor meta-repo  
**Artifact:** `CONTRIBUTING.md` (§ When do I write an ADR?, § What evidence is required?)  
**Date extracted:** 2026-07-09

## What happened?

Contributor guide defines when to write ADRs, what evidence is required per change type, and proposal gates for framework changes.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Ongoing contributor policy — not a single recorded decision | recording threshold |
| What evidence existed? | Distilled from ADR-001/002 practice | evidence source |
| What alternatives were rejected? | Not documented | — |
| How was confidence expressed? | Evidence table by change type; immutability rule stated | confidence expression |
| How could this be superseded? | New ADR or CONTRIBUTING revision | supersession trigger |
| What governance rule is implicit? | ADR when decision constrains future work; framework change needs 2 independent projects | recording threshold |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Friction evidence | Handoff friction log (referenced) | No |
| Policy rules | CONTRIBUTING tables | Yes |
| ADR format reference | Link to ADR-001 | No |

## Primitive chain

```text
CONTRIBUTING.md
  → Recording threshold: "constrains future work"
  → Evidence requirements vary by change type (contract, Skill, Experience claim, etc.)
  → Framework changes: same friction in two independent projects
  → Proposal gate: three questions before framework addition
  → ADR immutability; supersede for changes
```

## Notes

Meta-governance lives in contributor docs, not in ADR index. Parallel to portfolio ADR-008 pattern.
