# ADR-002: Portfolio Rich Template as Primary Spec Shape

## Status
**Status:** Accepted  
**Date:** 2026-07-10  
**Decision Maker(s):** Project maintainer  
**Supersedes:** None

## Context

The captured practice spans two corpora: jon-ohio-portfolio (80+ ADRs, full template from ADR-001) and Anchor (lean ADR contract, evolution evidence separate). The specification must choose a primary serialization shape while documenting the Anchor variant as a subset.

**In scope:** Default ADR template tier for `spec/adr-v1.0.md` and this reference implementation.  
**Out of scope:** Requiring POSITION papers or release evidence windows for all adopters.

## Decision Drivers

- Portfolio demonstrates mature practice at scale (index, LOG, typed relationships)
- Anchor lean contract is valid for early-stage or framework repos
- Spec must be implementable without mandating all portfolio infrastructure day one

## Options Considered

### Option A: Anchor minimal as primary spec
- **Description:** Tier 0 only; Context, Decision, Consequences, Options.
- **Pros:** Lower adoption barrier; matches CONTRIBUTING contract
- **Cons:** Under-specifies what portfolio proved necessary at scale; loses typed relationships, risks table as default
- **Effort:** Low

### Option B: Portfolio rich as primary; Anchor as documented variant
- **Description:** Tier 1 as recommended default in spec; Tier 0 + Anchor extensions as variant section.
- **Pros:** Matches highest-maturity corpus; tier guide lets adopters start minimal
- **Cons:** Heavier template may intimidate small projects
- **Effort:** Medium

### Option C: New hybrid template not observed in either corpus
- **Description:** Merge best-of both with new sections.
- **Cons:** Violates evidence-first derivation; invents rather than packages
- **Effort:** High

## Decision

**We will use Option B because the specification must serialize observed practice, and portfolio is the richest mature expression of that practice.**

Anchor variant documented in spec §10 and model §11. Adopters choose tier via selection guide; no cardinality rules in v1.0.

## Consequences

### Positive
- Reference implementation dogfoods Tier 1 (this ADR set)
- Index + LOG patterns available for scale
- Anchor adopters have explicit subset path

### Negative / Trade-offs
- Small projects may start Tier 0 and upgrade later (observed Anchor maturity curve)

### Operational Impact
- `spec/adr-v1.0.md` Tier 1 sections are normative for full conformance
- **Migration / rollback:** Adopters on Anchor contract need not adopt index/LOG

### Risks

| Risk | Likelihood | Impact | Mitigation | Owner/Role | Review Trigger |
|------|-----------|--------|------------|------------|----------------|
| Tier 1 perceived as mandatory | Med | Low | Tier selection guide in spec §9 | Maintainer | Validation feedback |

## Review Schedule
- **Next review:** After validation adoption attempt
- **Review owner:** Project maintainer

## Related ADRs
- [ADR-001](ADR-001-evidence-first-derivation-methodology.md) — depends on
- [ADR-003](ADR-003-recording-threshold-for-this-repo.md) — constrains

## References
- [discovery/synthesis/divergent-patterns.md](../discovery/synthesis/divergent-patterns.md)
- [model/adr-practice-model-v1.0.md](../model/adr-practice-model-v1.0.md) §10–11
- [spec/adr-v1.0.md](../spec/adr-v1.0.md)
