# Governance Primitives

**Status:** Discovery Phase 1 synthesis  
**Date:** 2026-07-09  
**Corpus:** Anchor meta-repo (7 extractions) + jon-ohio-portfolio (9 extractions)

Descriptive only. Primitives marked **convergent** appear in both corpora with consistent behaviour. Primitives marked **partial** appear in both but with different expression. **Single-corpus** primitives appear in one corpus only.

---

## Primitive catalog

| Primitive | Definition | Convergence | Evidence count |
|-----------|------------|-------------|----------------|
| recording threshold | Condition that triggers a durable decision record | **Convergent** | Anchor: ADR-001/002/003, CONTRIBUTING, POSITION; Portfolio: ADR-008, 079, all samples |
| evidence source | Where supporting material lived before/during the decision | **Partial** | Both: narrative + external refs; Anchor adds separate evidence.md layer |
| rejected alternatives preserved | Rejected options documented with rationale | **Convergent** | All ADR extractions in both corpora |
| confidence expression | How certainty is communicated (status, risks, criteria) | **Convergent** | Mature ADRs in both: Accepted + risks; portfolio adds success criteria (ADR-069) |
| supersession trigger | How and when a decision is replaced | **Convergent** | Both: immutability + new ADR; portfolio adds index Superseded By |
| decision ownership | Named owner of decision and consequences | **Convergent** | Metadata in all sampled ADRs |
| review trigger | Scheduled or event-driven re-evaluation | **Convergent** | ADR-002/003, portfolio ADR-001/008/069/073/079 |
| scope boundary | Explicit in-scope / out-of-scope limits | **Partial** | Portfolio: all samples; Anchor: ADR-002/003 only |
| relationship typing | Typed links between decisions (depends, supersedes, constrains, amends) | **Partial** | Portfolio: explicit verbs; Anchor: informal Related ADRs |
| meta-governance record | ADR or policy defining when ADRs are required | **Partial** | Portfolio ADR-008; Anchor CONTRIBUTING (not ADR) |
| governance infrastructure | Artifacts beyond individual ADRs (index, log, evidence window) | **Single-corpus each** | Portfolio: index + LOG; Anchor: evidence.md + POSITION + coordination-problem |
| pre-decision investigation | Hypothesis + evidence table before capability/decision promotion | **Single-corpus** | Anchor coordination-problem TEMPLATE |
| gated promotion artifact | Proposed status with explicit path to Accepted ADR | **Single-corpus** | Anchor POSITION paper |
| decision bundling | Multiple related decisions in one ADR | **Single-corpus** | Portfolio ADR-073 |
| stale rationale marking | Explicit note when prior ADR rationale is outdated | **Single-corpus** | Portfolio ADR-079 (ADR-055 stale) |

---

## Convergence assessment

**Strongly convergent (7 primitives):** recording threshold, rejected alternatives preserved, confidence expression, supersession trigger, decision ownership, review trigger, and the immutability norm.

**Partially convergent (4 primitives):** evidence source, scope boundary, relationship typing, meta-governance record — same concept, different artifacts or expression depth.

**Corpus-specific (4 patterns):** governance infrastructure shape, pre-decision investigation, gated promotion artifacts, decision bundling.

---

## Discovery gate

**Question:** Enough convergent primitives to draft Governance Model v1.0?

**Answer:** **Yes — partial-strong convergence.**

Seven primitives recur across independent corpora with consistent behaviour. Four partial primitives are model parameters (how evidence is stored, how relationships are typed), not absences. Corpus-specific patterns are extensions the model may optionalize rather than require.

**Hypothesis status:** A reusable governance model **likely emerges** — not proven until Governance Model v1.0 is drafted and validated. Alternative outcome (too project-specific) remains possible if v1.0 cannot unify partial primitives without arbitrary choices.

---

## Primitive recurrence map

```text
recording threshold
  ← Anchor ADR-001, ADR-002, ADR-003, CONTRIBUTING, POSITION
  ← Portfolio ADR-001, ADR-008, ADR-079

rejected alternatives preserved
  ← All ADR extractions (both corpora)

supersession trigger
  ← Anchor ADR-001, ADR-002, ADR-003
  ← Portfolio ADR-025→026, ADR-079, index.md

confidence expression (risks + status)
  ← Anchor ADR-001, ADR-002, ADR-003
  ← Portfolio ADR-001, ADR-008, ADR-069, ADR-073, ADR-079

review trigger
  ← Anchor ADR-002, ADR-003, governance.md
  ← Portfolio ADR-001, ADR-008, ADR-069, ADR-073, ADR-079

decision ownership
  ← All sampled ADRs (both corpora)
```

---

## Next step

Draft `governance-model/v1.0.md` from convergent and partial primitives. Defer specification until model is written.
