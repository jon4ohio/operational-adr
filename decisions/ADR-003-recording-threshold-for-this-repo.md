# ADR-003: Recording Threshold for This Repository

## Status
**Status:** Accepted  
**Date:** 2026-07-10  
**Decision Maker(s):** Project maintainer  
**Supersedes:** None

## Context

This repository documents and packages an ADR practice. It must practice what it specifies: durable records when decisions constrain future work. Without a recording threshold, model/spec choices would live only in chat or CHARTER prose.

**In scope:** When to add ADRs under `decisions/` in evidence-first-adr.  
**Out of scope:** Adopter projects' thresholds (they choose ADR or policy per spec §5).

## Decision Drivers

- Meta-governance must be exemplified, not only described
- Portfolio ADR-008 pattern: major structural choices get ADRs
- Anchor CONTRIBUTING pattern: ADR when decision constrains future work

## Options Considered

### Option A: CHARTER only (no meta-governance ADR)
- **Description:** Recording rules live in CHARTER.md; no ADR-008 equivalent.
- **Pros:** Fewer files
- **Cons:** CHARTER mixes purpose with operational rules; portfolio proved ADR works for meta-governance
- **Effort:** Low

### Option B: Meta-governance ADR (this document + ADR-001/002 for major choices)
- **Description:** ADR when packaging choice constrains model, spec, or reference implementation.
- **Pros:** Dogfoods portfolio pattern; immutable audit trail for packaging decisions
- **Cons:** Small repo may have few ADRs
- **Effort:** Low

## Decision

**We will use Option B.** Write an ADR in this repository when a decision:

1. Constrains the model, specification, or reference implementation shape
2. Chooses between observed corpus variants (e.g., portfolio vs Anchor primary)
3. Defines methodology adopters inherit (e.g., evidence-first derivation)

Routine doc fixes, typo corrections, and extraction updates do not require ADRs.

## Consequences

### Positive
- Reference implementation demonstrates meta-governance ADR pattern
- Packaging decisions (ADR-001, ADR-002) are supersession-ready

### Negative / Trade-offs
- Low ADR count may look sparse; index still valuable as project grows

### Operational Impact
- New packaging decisions → new ADR under `decisions/`
- **Migration / rollback:** N/A — greenfield meta-governance

### Risks

| Risk | Likelihood | Impact | Mitigation | Owner/Role | Review Trigger |
|------|-----------|--------|------------|------------|----------------|
| Over-ADR-ing trivial changes | Low | Low | Threshold list above | Maintainer | Review at 10+ ADRs |

## Review Schedule
- **Next review:** When first supersession occurs or at 10 ADRs
- **Review owner:** Project maintainer

## Related ADRs
- [ADR-001](ADR-001-evidence-first-derivation-methodology.md) — follow-up
- [ADR-002](ADR-002-portfolio-primary-spec-shape.md) — follow-up

## References
- [discovery/extraction/portfolio/ADR-008-extraction.md](../discovery/extraction/portfolio/ADR-008-extraction.md)
- [discovery/extraction/anchor/CONTRIBUTING-evidence-extraction.md](../discovery/extraction/anchor/CONTRIBUTING-evidence-extraction.md)
- [spec/adr-v1.0.md](../spec/adr-v1.0.md) §5
