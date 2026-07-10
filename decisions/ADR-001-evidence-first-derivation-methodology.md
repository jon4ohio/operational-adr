# ADR-001: Evidence-First Derivation Methodology

## Status
**Status:** Accepted  
**Date:** 2026-07-10  
**Decision Maker(s):** Project maintainer  
**Supersedes:** None

## Context

This project packages an existing ADR practice from years of use across portfolio and Anchor repositories. At inception the work drifted toward inventing a universal governance framework. Clarification restored the original intent: capture what works, make it adoptable.

**In scope:** How this repository derives its model and specification.  
**Out of scope:** Mandating inline evidence tables in every adopters' ADRs; comparison with Nygard/MADR as normative.

## Decision Drivers

- Adopters must trust the spec is derived, not invented
- Phase 1 capture (16 extractions, synthesis) is complete and should not be re-run
- "Evidence-first" must name methodology, not a per-ADR content requirement

## Options Considered

### Option A: Design specification from first principles
- **Description:** Compare Nygard/MADR, synthesize best practices, write spec without corpus extraction.
- **Pros:** Faster; familiar to ADR community
- **Cons:** Contradicts lived practice; loses provenance; repeats governance-theory drift
- **Effort:** Low

### Option B: Evidence-first derivation (observe → extract → model → specify)
- **Description:** Capture existing practice, map extractions to model elements via traceability, derive spec from model.
- **Pros:** Provenance auditable; preserves practice fidelity; differentiator is methodological honesty
- **Cons:** More upfront work; requires access to source corpora during capture
- **Effort:** Medium

## Decision

**We will use Option B because provenance makes the practice adoptable without the author's private repositories.**

Architecture:

```text
Existing ADR Practice (discovery/)
  → model/traceability.md
  → model/adr-practice-model-v1.0.md
  → spec/adr-v1.0.md
  → decisions/ (reference implementation)
```

Evidence for this decision lives in `discovery/` (extractions + synthesis), not inline in this ADR.

## Consequences

### Positive
- Every model element traceable via `model/traceability.md`
- Model and spec change only when capture evidence contradicts them
- Clear answer to "how do I know you didn't just invent this?"

### Negative / Trade-offs
- Capture phase is a one-time dependency; new corpora require new extraction cycle to extend provenance

### Operational Impact
- Phase 1 deliverables are frozen; Phase 2+ builds on synthesis
- **Migration / rollback:** Revert to first-principles spec would discard `discovery/` provenance chain

### Risks

| Risk | Likelihood | Impact | Mitigation | Owner/Role | Review Trigger |
|------|-----------|--------|------------|------------|----------------|
| Provenance map incomplete | Low | High | traceability.md maps all 16 extractions | Maintainer | New extraction added |
| "Evidence-first" misread as inline mandate | Med | Med | README + this ADR clarify methodology | Maintainer | Adopter feedback |

## Review Schedule
- **Next review:** After first external adoption attempt (see `validation/log.md`)
- **Review owner:** Project maintainer

## Related ADRs
- [ADR-002](ADR-002-portfolio-primary-spec-shape.md) — depends on: primary template choice
- [ADR-003](ADR-003-recording-threshold-for-this-repo.md) — constrains: when to add ADRs here

## References
- [CHARTER.md](../CHARTER.md)
- [discovery/synthesis/governance-primitives.md](../discovery/synthesis/governance-primitives.md)
- [model/traceability.md](../model/traceability.md)
- Product identity: published as Operational ADR (formerly Evidence-First ADR); this ADR records derivation methodology only
