# Extraction — Anchor ADR-001

**Corpus:** Anchor meta-repo  
**Artifact:** `docs/decisions/ADR-001-contracts-not-artifacts.md`  
**Date extracted:** 2026-07-09

## What happened?

After extended design discussion, Anchor froze v0.1 as seven contracts and four principles, ending the design phase and beginning validation across three projects.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Design phase reached diminishing returns; further discussion would optimize specification without validating practice | recording threshold |
| What evidence existed? | Extended design conversation; competing directions enumerated in Context; empirical questions unresolved by theory | evidence source |
| What alternatives were rejected? | Options A–D documented with pros/cons/effort; D chosen | rejected alternatives preserved |
| How was confidence expressed? | Status Accepted; risks table with likelihood/impact/mitigation/owner/review trigger | confidence expression |
| How could this be superseded? | Operational Impact: "supersede this ADR with one that documents what changed and why" | supersession trigger |
| What governance rule is implicit? | ADRs only for decisions constraining future work; Skills/Playbooks promoted after repetition | recording threshold, review trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Design discussion | Referenced in Context and References; not linked | Partially |
| Competing directions | Context section | Yes |
| Validation plan | Decision body (three projects) | Yes |

## Primitive chain

```text
ADR-001
  → Recording threshold: design diminishing returns + need to validate in practice
  → Evidence source: design conversations (implicit, not tabulated)
  → Alternatives preserved: four options with structured comparison
  → Confidence expression: Accepted + risks table
  → Supersession trigger: explicit supersede path in Operational Impact
  → Decision ownership: Project maintainer (metadata)
```

## Notes

No Decision Drivers, Review Schedule, or in/out of scope sections. Governance metadata lighter than later Anchor ADRs.
