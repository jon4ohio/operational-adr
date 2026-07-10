# Extraction — Portfolio ADR-001

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/ADR-001-inline-styles-for-layout-and-visuals.md`  
**Date extracted:** 2026-07-09

## What happened?

Documented existing inline-style convention for layout/visuals; Tailwind limited to animation utilities.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Repo already used inline styles; need stable convention for future edits | recording threshold |
| What evidence existed? | Observed repo convention; CLAUDE.md architecture reference | evidence source |
| What alternatives were rejected? | Option B (Tailwind for layout) with pros/cons/effort | rejected alternatives preserved |
| How was confidence expressed? | Accepted; risks table; Review Schedule | confidence expression |
| How could this be superseded? | "Create new ADR that supersedes this one and migrate incrementally" | supersession trigger |
| What governance rule is implicit? | Document convention before it drifts; Related ADRs constrain scope | recording threshold, scope boundary |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Existing convention | Context + CLAUDE.md reference | Partially |
| Alternative approach | Options section | Yes |

## Primitive chain

```text
ADR-001 (portfolio)
  → Recording threshold: codify existing practice before drift
  → Evidence source: repo state + contributor docs
  → Scope boundary: In scope / Out of scope
  → Alternatives preserved: Option A vs B
  → Confidence expression: risks + scheduled review
  → Supersession trigger: explicit new ADR path
  → Decision ownership: John Ohio (Owner/Maintainer)
```

## Notes

Foundational portfolio ADR. Full governance metadata from first record.
