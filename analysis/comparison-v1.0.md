# Peer Comparison v1.0

**Status:** Optional validation artifact  
**Date:** 2026-07-10

Descriptive comparison of Evidence-First ADR with common ADR formats. **Not normative** — does not reshape capture, model, or spec.

---

## Influences and lineage

Evidence-First ADR does not claim to invent architectural decision records. It packages a practice with acknowledged influences:

| Influence | Role |
|-----------|------|
| **Nygard ADRs** | Foundational pattern (Context, Decision, Status, Consequences) |
| **MADR** | Community markdown template; minimal/full modes |
| **Future Friendly Decision** | Conceptual influence on decision durability and review (acknowledged; not part of Phase 1 extraction corpus) |
| **jon-ohio-portfolio** | Primary extraction corpus (80+ ADRs, index, LOG, typed relationships) |
| **Anchor** | Secondary extraction corpus (lean contract, ecosystem patterns) |

Phase 1 provenance in [model/traceability.md](../model/traceability.md) maps only portfolio and Anchor extractions. Nygard, MADR, and Future Friendly Decision appear here as lineage—not as extracted evidence.

---

## Comparison matrix

| Aspect | Nygard (classic) | MADR | Evidence-First ADR v1.0 |
|--------|------------------|------|------------------------|
| Origin | Written as pattern | Written as template | Extracted from lived practice (portfolio + Anchor) |
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

## What Evidence-First ADR adds (from practice, not invention)

1. **Traceability chain** — extractions → model elements → spec sections
2. **Tier system** — Tier 0 (Anchor lean) through Tier 2 (infrastructure extensions)
3. **Evidence ecosystem** — index, LOG, release evidence, POSITION papers as optional artifacts
4. **Relationship typing** — depends on, supersedes, constrains, amends (portfolio at scale)
5. **Methodological claim** — spec derived from observed practice, not first principles

---

## What Evidence-First ADR does not claim

- Superiority over Nygard or MADR for all projects
- Universal governance framework
- Mandatory evidence tables inside every ADR
- Cardinality or validation rules beyond observed practice

---

## Adoption guidance

| If you already use… | Consider… |
|--------------------|-----------|
| Nygard minimal | Evidence-First Tier 0 — similar shape, adds supersession + optional tiers |
| MADR | Evidence-First Tier 1 — comparable richness; add traceability mindset if packaging practice |
| No ADRs | Start Tier 0; add index at 10+ ADRs per spec §6 |

---

## References

- Michael Nygard — Documenting Architecture Decisions
- MADR — Markdown Architectural Decision Records
- [model/adr-practice-model-v1.0.md](../model/adr-practice-model-v1.0.md)
- [validation/log.md](../validation/log.md)
