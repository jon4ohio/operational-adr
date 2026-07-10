# Extraction — Anchor POSITION-coordination-architecture

**Corpus:** Anchor meta-repo  
**Artifact:** `docs/decisions/POSITION-anchor-coordination-architecture.md`  
**Date extracted:** 2026-07-09

## What happened?

A proposed architectural position paper generalizes session-arbitration to coordination architecture identity. Status is Proposed — not Accepted. Explicit governance path defined before ADR promotion.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Context-arbitration experiment (Sessions 0–5) demonstrated capability; architecture identity not yet supported | recording threshold |
| What evidence existed? | Experiment log, maintainer observations, comparative implementation assessments; independent adopters pending | evidence source |
| What alternatives were rejected? | Not framed as options; "What is not Anchor" boundary list | scope boundary |
| How was confidence expressed? | Status Proposed; "Supported now" vs "Not supported yet" split; Evidence reviewed section with date | confidence expression |
| How could this be superseded? | Governance path: Evidence Review → accepted → adopter gate → ADR if supported | supersession trigger |
| What governance rule is implicit? | Identity claims require Evidence Review + independent adopter; not an ADR until gated | recording threshold, review trigger |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Experiment results | context-arbitration-experiment.md | No (linked) |
| Evidence summary | "Evidence reviewed" section | Yes (pointer) |
| Promotion criteria | Governance path header | Yes |

## Primitive chain

```text
POSITION-anchor-coordination-architecture
  → Recording threshold: empirical trigger (experiment) without identity claim
  → Evidence source: external experiment log + dated evidence review
  → Artifact type: POSITION (not ADR) until gate satisfied
  → Confidence expression: Proposed status; split supported/unsupported claims
  → Review trigger: Evidence Review + independent adopter gate
  → Supersession trigger: promotion to ADR only if evidence supports
```

## Notes

Governance behaviour distinct from ADR: pre-decision artifact with explicit promotion path. Evidence lives primarily outside the document.
