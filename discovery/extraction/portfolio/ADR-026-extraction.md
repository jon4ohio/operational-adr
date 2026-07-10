# Extraction — Portfolio ADR-026

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/ADR-026-orchestrated-portfolio-case-study-narrative-refresh.md`  
**Date extracted:** 2026-07-09

## What happened?

Superseded ADR-025. Refreshed case study narrative to first-person orchestration; shortened subtitle.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Copy read as tooling inventory vs orchestration story; subtitle still too long after ADR-025 | recording threshold |
| What evidence existed? | Prior copy state; decision log as grounding source (ADR-008 reference) | evidence source |
| What alternatives were rejected? | Option A (minimal edits) vs Option B (full narrative refresh) | rejected alternatives preserved |
| How was confidence expressed? | Accepted; risks table; Review Schedule | confidence expression |
| How could this be superseded? | Revert lib/projects.ts + supersede this ADR to restore ADR-025 decision | supersession trigger |
| What governance rule is implicit? | ADR-008 gate; decision log as governance mechanism | recording threshold, review trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Prior ADR | ADR-025 (supersedes relationship) | No (link) |
| Build history | Risk mitigation: verify against commit history | No |
| Decision log | ADR-008 dependency cited | No |

## Primitive chain

```text
ADR-026
  → Recording threshold: narrative quality insufficient after ADR-025
  → Supersedes ADR-025 (explicit metadata)
  → Evidence source: decision log + commit history (external)
  → Depends on ADR-008 (meta-governance)
  → Rollback path documented in Operational Impact
```

## Notes

Supersession chain ADR-025 → ADR-026 visible in index and Related ADRs.
