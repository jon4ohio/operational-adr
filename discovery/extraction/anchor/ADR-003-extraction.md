# Extraction — Anchor ADR-003

**Corpus:** Anchor meta-repo  
**Artifact:** `docs/decisions/ADR-003-product-narrative.md`  
**Date extracted:** 2026-07-09

## What happened?

Anchor v0.2 shipped a responsibility-first product layer, frozen phrases, orient-project playbook, and teach-vs-claim Experience governance tied to Release Governance.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Adoption validation: strangers sent to Entry before understanding value; framework-first README bounce | recording threshold |
| What evidence existed? | Adoption validation observations; design discussions; ADR-002 split incomplete for product layer | evidence source |
| What alternatives were rejected? | Options A–C (framework-first README, responsibility-first, external journey repo) | rejected alternatives preserved |
| How was confidence expressed? | Accepted; teach-vs-claim rule; risks table; Review Schedule tied to Evidence Review completion | confidence expression |
| How could this be superseded? | "Supersede with ADR if responsibility-first product layer fails evidence review" | supersession trigger |
| What governance rule is implicit? | Normative claims require validation evidence; structural changes wait for Evidence Review | recording threshold, review trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Adoption validation | Context (narrative) | Partially |
| Release governance | Links to releases/governance.md | No |
| Frozen vocabulary | Decision body | Yes |

## Primitive chain

```text
ADR-003
  → Recording threshold: validated adoption friction (wrong audience order)
  → Evidence source: adoption validation + prior ADR chain
  → Scope boundary: In scope / Out of scope (no eighth contract, no Entry §4 rewrite)
  → Alternatives preserved: three product-layer options
  → Confidence expression: teach-vs-claim + scheduled review at Evidence Review
  → Supersession trigger: conditional on evidence review failure
  → Links to external governance: Release Governance layer referenced
```

## Notes

Decision explicitly defers normative claims to validation evidence while shipping descriptive teaching content.
