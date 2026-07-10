# Traceability

**Status:** Phase 2 — provenance for ADR Practice Model v1.0  
**Date:** 2026-07-10

Answers: *How do I know this model wasn't invented?*

Every model element maps to capture evidence in [`discovery/`](../discovery/). The specification is derived from this provenance—not from first principles.

---

## Model elements → extractions

### Recording threshold

When a durable ADR is required.

| Extraction | Observation |
|------------|-------------|
| [anchor/ADR-001](../discovery/extraction/anchor/ADR-001-extraction.md) | Design diminishing returns → freeze and validate |
| [anchor/ADR-002](../discovery/extraction/anchor/ADR-002-extraction.md) | Recurring architectural tension (framework vs product) |
| [anchor/ADR-003](../discovery/extraction/anchor/ADR-003-extraction.md) | Adoption validation friction (wrong audience order) |
| [anchor/CONTRIBUTING-evidence](../discovery/extraction/anchor/CONTRIBUTING-evidence-extraction.md) | ADR when decision "constrains future work" |
| [anchor/POSITION-coordination-architecture](../discovery/extraction/anchor/POSITION-coordination-architecture-extraction.md) | Experiment demonstrated capability → gated position |
| [portfolio/ADR-001](../discovery/extraction/portfolio/ADR-001-extraction.md) | Codify existing convention before drift |
| [portfolio/ADR-008](../discovery/extraction/portfolio/ADR-008-extraction.md) | **Meta:** major push requires ADR action |
| [portfolio/ADR-079](../discovery/extraction/portfolio/ADR-079-extraction.md) | IA change triggers ADR-008 gate |

---

### Rejected alternatives preserved

Rejected options remain documented with rationale.

| Extraction | Observation |
|------------|-------------|
| All 16 ADR extractions | Options Considered with pros/cons in both corpora |
| [anchor/ADR-001](../discovery/extraction/anchor/ADR-001-extraction.md) | Four options A–D |
| [portfolio/ADR-025](../discovery/extraction/portfolio/ADR-025-extraction.md) | Option A vs B for card copy |
| [portfolio/ADR-073](../discovery/extraction/portfolio/ADR-073-extraction.md) | Options A–E per sub-decision |

---

### Confidence expression

Status, risks, and optional success criteria make acceptance auditable.

| Extraction | Observation |
|------------|-------------|
| [anchor/ADR-001](../discovery/extraction/anchor/ADR-001-extraction.md) | Accepted + risks table |
| [anchor/ADR-002](../discovery/extraction/anchor/ADR-002-extraction.md) | Drivers + risks + review schedule |
| [portfolio/ADR-001](../discovery/extraction/portfolio/ADR-001-extraction.md) | Full metadata from first ADR |
| [portfolio/ADR-069](../discovery/extraction/portfolio/ADR-069-extraction.md) | Explicit success criteria in Decision |

---

### Supersession trigger

Immutability; new ADR replaces old; chain preserved.

| Extraction | Observation |
|------------|-------------|
| [anchor/ADR-001](../discovery/extraction/anchor/ADR-001-extraction.md) | Supersede path in Operational Impact |
| [anchor/CONTRIBUTING-evidence](../discovery/extraction/anchor/CONTRIBUTING-evidence-extraction.md) | Immutability rule stated |
| [portfolio/ADR-025](../discovery/extraction/portfolio/ADR-025-extraction.md) | Status: Superseded by ADR-026 |
| [portfolio/ADR-026](../discovery/extraction/portfolio/ADR-026-extraction.md) | Supersedes ADR-025 |
| [portfolio/ADR-079](../discovery/extraction/portfolio/ADR-079-extraction.md) | Supersedes ADR-041 in effect; amends ADR-075 |
| [portfolio/index](../discovery/extraction/portfolio/index-extraction.md) | Superseded By column at scale |

---

### Decision ownership

Named owner in metadata.

| Extraction | Observation |
|------------|-------------|
| All sampled ADR extractions (both corpora) | Decision Maker(s) field |

---

### Review trigger

Scheduled or event-driven re-evaluation.

| Extraction | Observation |
|------------|-------------|
| [anchor/ADR-002](../discovery/extraction/anchor/ADR-002-extraction.md) | Review after portfolio/greenfield validation |
| [anchor/ADR-003](../discovery/extraction/anchor/ADR-003-extraction.md) | Review at Evidence Review completion |
| [portfolio/ADR-008](../discovery/extraction/portfolio/ADR-008-extraction.md) | Review Schedule 2026-07-10 |
| [portfolio/ADR-073](../discovery/extraction/portfolio/ADR-073-extraction.md) | Review on case study publish or date |

---

### Evidence references (ecosystem)

Evidence lives outside ADR; ADR points to it.

| Extraction | Observation |
|------------|-------------|
| [anchor/ADR-001](../discovery/extraction/anchor/ADR-001-extraction.md) | Design conversation in Context |
| [anchor/governance-md](../discovery/extraction/anchor/governance-md-extraction.md) | Observations in evidence.md, separate from ADRs |
| [anchor/POSITION-coordination-architecture](../discovery/extraction/anchor/POSITION-coordination-architecture-extraction.md) | Experiment log external |
| [portfolio/ADR-026](../discovery/extraction/portfolio/ADR-026-extraction.md) | Commit history for verification |
| [portfolio/ADR-073](../discovery/extraction/portfolio/ADR-073-extraction.md) | PR #178, #179 in References |
| [portfolio/LOG](../discovery/extraction/portfolio/LOG-extraction.md) | Chronological acceptance audit |

**Synthesis:** [evidence-location-map](../discovery/synthesis/evidence-location-map.md) — neither corpus mandates inline evidence tables.

---

### Scope boundary

Explicit in-scope / out-of-scope.

| Extraction | Observation |
|------------|-------------|
| [anchor/ADR-002](../discovery/extraction/anchor/ADR-002-extraction.md) | In scope / Out of scope sections |
| [anchor/ADR-003](../discovery/extraction/anchor/ADR-003-extraction.md) | No eighth contract, no Entry rewrite |
| All portfolio ADR samples | In scope / Out of scope in every sampled ADR |

---

### Relationship typing

Typed links between decisions.

| Extraction | Observation |
|------------|-------------|
| [anchor/ADR-002](../discovery/extraction/anchor/ADR-002-extraction.md) | Related ADRs — informal list |
| [portfolio/ADR-026](../discovery/extraction/portfolio/ADR-026-extraction.md) | depends on, supersedes, constrains |
| [portfolio/ADR-079](../discovery/extraction/portfolio/ADR-079-extraction.md) | depends on, supersedes, constrains, amends; stale rationale noted |

---

### Meta-governance (when to write ADRs)

| Extraction | Observation |
|------------|-------------|
| [portfolio/ADR-008](../discovery/extraction/portfolio/ADR-008-extraction.md) | Meta-governance as ADR |
| [anchor/CONTRIBUTING-evidence](../discovery/extraction/anchor/CONTRIBUTING-evidence-extraction.md) | Meta-governance as contributor policy |

**Model parameter:** ADR or policy document—both valid.

---

### Supporting infrastructure (optional extensions)

| Extraction | Model element |
|------------|---------------|
| [portfolio/index](../discovery/extraction/portfolio/index-extraction.md) | Decision index with status + Superseded By |
| [portfolio/LOG](../discovery/extraction/portfolio/LOG-extraction.md) | Chronological ADR audit log |
| [anchor/governance-md](../discovery/extraction/anchor/governance-md-extraction.md) | Evolution evidence window (Anchor variant) |
| [anchor/coordination-problem-template](../discovery/extraction/anchor/coordination-problem-template-extraction.md) | Pre-decision investigation (Tier 1 optional) |
| [anchor/POSITION-coordination-architecture](../discovery/extraction/anchor/POSITION-coordination-architecture-extraction.md) | Gated promotion artifact (Anchor variant) |

---

### Optional patterns (single-corpus)

| Extraction | Pattern | Model treatment |
|------------|---------|-----------------|
| [portfolio/ADR-073](../discovery/extraction/portfolio/ADR-073-extraction.md) | Decision bundling | Allowed with explicit sub-decisions |
| [portfolio/ADR-079](../discovery/extraction/portfolio/ADR-079-extraction.md) | Stale rationale marking | Recommended at scale |

---

## Extraction → model element (summary table)

| Extraction | Primary model elements |
|------------|------------------------|
| anchor/ADR-001 | Recording threshold, alternatives, confidence, supersession |
| anchor/ADR-002 | Recording threshold, alternatives, confidence, review, scope, relationships |
| anchor/ADR-003 | Recording threshold, alternatives, confidence, review, scope |
| anchor/POSITION-coordination-architecture | Recording threshold, evidence refs, gated promotion |
| anchor/governance-md | Evidence ecosystem, review at project level |
| anchor/coordination-problem-template | Pre-decision investigation (optional) |
| anchor/CONTRIBUTING-evidence | Recording threshold, meta-governance, supersession |
| portfolio/ADR-001 | Recording threshold, alternatives, confidence, review, scope |
| portfolio/ADR-008 | **Meta-governance**, recording threshold, review |
| portfolio/ADR-025 | Alternatives, supersession chain |
| portfolio/ADR-026 | Alternatives, supersession, evidence refs |
| portfolio/ADR-069 | Alternatives, confidence (success criteria), scope |
| portfolio/ADR-073 | Bundling, alternatives, relationships, evidence refs |
| portfolio/ADR-079 | Recording threshold, relationships, stale rationale, supersession |
| portfolio/index | Supersession infrastructure |
| portfolio/LOG | Audit infrastructure |

---

## Lifecycle provenance

The convergent lifecycle in [adr-practice-model-v1.0.md](adr-practice-model-v1.0.md) derives from [convergent-patterns.md](../discovery/synthesis/convergent-patterns.md), which synthesizes all 16 extractions.

```text
Threshold met          ← ADR-008, CONTRIBUTING, ADR-001, ADR-079
Evidence gathered      ← evidence-location-map (external refs)
Alternatives preserved ← all ADR extractions
Decision accepted      ← confidence expression extractions
Review scheduled       ← ADR-002, ADR-003, portfolio review schedules
Supersession defined   ← ADR-001, ADR-025/026, index
Immutability enforced  ← CONTRIBUTING, portfolio supersession chain
```
