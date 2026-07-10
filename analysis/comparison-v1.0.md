# Peer Comparison v1.0

**Status:** Optional validation artifact  
**Date:** 2026-07-10

Descriptive comparison of Operational ADR (formerly published as Evidence-First ADR) with common ADR formats. **Not normative** — does not reshape capture, model, or spec.

---

## Influences

Operational ADR does not claim to invent architectural decision records. Acknowledged **influences** (ideas):

| Influence | Role |
|-----------|------|
| **Nygard ADRs** | Foundational pattern (Context, Decision, Status, Consequences) |
| **MADR** | Community markdown template; minimal/full modes |
| **Future Friendly Decision** | Conceptual influence on decision durability and review (not part of Phase 1 extraction corpus) |

## Extraction provenance

**Provenance** (Phase 1 capture only—why v1.0 looks like this; not adoption prerequisites):

| Source | Role |
|--------|------|
| **jon-ohio-portfolio** | Primary extraction corpus (80+ ADRs, index, LOG, typed relationships) |
| **Anchor** | Secondary extraction corpus (lean contract, ecosystem patterns) |

Portfolio and Anchor are not ecosystem members for adopters. They document origin. See [discovery/](../discovery/) and [model/traceability.md](../model/traceability.md). Going forward, Anchor is one adopter among many.

---

## Comparison matrix

| Aspect | Nygard (classic) | MADR | Operational ADR v1.0 |
|--------|------------------|------|------------------------|
| Origin | Written as pattern | Written as template | Extracted from lived practice; provenance in [traceability.md](../model/traceability.md)—adopters need not access source repos |
| Provenance | Author intent | Community template | [traceability.md](../model/traceability.md) maps 16 extractions |
| Core sections | Title, Context, Decision, Status, Consequences | Configurable; often Context, Decision, Consequences | Tier 0: same core; Tier 1: drivers, options, risks, review |
| Alternatives | Optional | Encouraged | Required when alternatives exist (observed in all corpus ADRs) |
| Immutability | Implied | Varies | Explicit: supersede, do not edit Accepted |
| Relationships | Informal | Optional links | Typed verbs at Tier 1 (portfolio); informal at Tier 0 |
| Index / LOG | Not specified | Not specified | Optional infrastructure from portfolio at scale |
| Evidence in ADR | Narrative | Varies | References external evidence; no inline table mandate |
| Meta-governance | Not specified | Not specified | ADR or policy doc (both observed) |
| Variants | Single shape | Minimal / full modes | Portfolio primary + Anchor subset documented |

---

## What Operational ADR adds (from practice, not invention)

1. **Traceability chain** — extractions → model elements → spec sections
2. **Tier system** — Tier 0 (Anchor lean) through Tier 2 (infrastructure extensions)
3. **Evidence ecosystem** — index, LOG, release evidence, POSITION papers as optional artifacts
4. **Relationship typing** — depends on, supersedes, constrains, amends (portfolio at scale)
5. **Methodological claim** — spec derived from observed practice, not first principles

---

## What Operational ADR does not claim

- Superiority over Nygard or MADR for all projects
- Universal governance framework
- Mandatory evidence tables inside every ADR
- Cardinality or validation rules beyond observed practice

---

## Adoption guidance

| If you already use… | Consider… |
|--------------------|-----------|
| Nygard minimal | Operational ADR Tier 0 — similar shape, adds supersession + optional tiers |
| MADR | Operational ADR Tier 1 — comparable richness; add traceability mindset if packaging practice |
| No ADRs | Start Tier 0; add index at 10+ ADRs per spec §6 |

---

## References

- Michael Nygard — Documenting Architecture Decisions
- MADR — Markdown Architectural Decision Records
- [model/adr-practice-model-v1.0.md](../model/adr-practice-model-v1.0.md)
- [validation/log.md](../validation/log.md)
