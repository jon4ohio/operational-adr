# Divergent Patterns

**Status:** Discovery Phase 1 synthesis  
**Date:** 2026-07-09

Patterns that differ between corpora or appear in one corpus only. These become **model parameters** or **optional extensions** — not failures of convergence.

---

## 1. Where evolution evidence lives

| Corpus | Pattern |
|--------|---------|
| Anchor | Framework/product evolution evidence in `releases/v0.2/evidence.md` — separate from ADRs |
| Portfolio | No equivalent release evidence window; friction captured in ADR-008 discipline + LOG |

**Divergence:** Anchor splits **project evolution governance** from **architectural decision records**. Portfolio folds governance into ADR discipline + index/LOG.

**Model implication:** Governance model may need two tiers — decision records vs evolution evidence — without requiring both in every project.

---

## 2. Meta-governance artifact type

| Corpus | Pattern |
|--------|---------|
| Anchor | CONTRIBUTING.md tables (not an ADR) |
| Portfolio | ADR-008 (meta-governance as ADR) |

**Divergence:** Same rule (when to write ADRs), different artifact choice.

**Model implication:** Meta-governance can be ADR or policy doc — model should not mandate one.

---

## 3. Governance infrastructure

| Corpus | Infrastructure |
|--------|----------------|
| Anchor | POSITION papers (pre-ADR gated), coordination-problem template, Handoff friction log |
| Portfolio | `index.md` (82+ rows, Superseded By), `LOG.md` (chronological audit) |

**Divergence:** Portfolio optimizes for **scale and supersession lookup**. Anchor optimizes for **pre-promotion investigation and release governance**.

**Model implication:** Reference implementation should support index + optional investigation log; not all adopters need POSITION papers or release windows.

---

## 4. Relationship typing depth

| Corpus | Pattern |
|--------|---------|
| Anchor | Related ADRs — informal list |
| Portfolio | Typed relationships: depends on, supersedes, constrains, amends; stale rationale noted |

**Divergence:** Portfolio at scale requires explicit relationship verbs and stale-rationale handling (ADR-079).

**Model implication:** Relationship types are optional tier — required for constraining decisions at scale.

---

## 5. Pre-decision evidence discipline

| Corpus | Pattern |
|--------|---------|
| Anchor | coordination-problem TEMPLATE: evidence table, falsification, Open/Supported/Not supported |
| Portfolio | Not observed in ADR corpus |

**Divergence:** Anchor's strongest evidence-first pattern governs **capability emergence**, not individual ADRs.

**Model implication:** Pre-decision evidence tables may apply to Tier 1 (constraining) decisions or framework changes — not every ADR.

---

## 6. Gated promotion artifacts

| Corpus | Pattern |
|--------|---------|
| Anchor | POSITION paper: Proposed → Evidence Review → ADR if supported |
| Portfolio | Not observed |

**Divergence:** Anchor defers identity-level claims behind evidence gates using non-ADR artifact type.

**Model implication:** Optional artifact type between investigation and ADR for high-stakes decisions.

---

## 7. Decision bundling

| Corpus | Pattern |
|--------|---------|
| Portfolio | ADR-073: three UX decisions in one ADR, shared branch/PR |
| Anchor | One strategic decision per ADR in samples |

**Divergence:** Portfolio bundles related decisions shipped together.

**Model implication:** Model may allow bundled decisions with explicit sub-decision structure.

---

## 8. Governance metadata maturity curve

| Corpus | Pattern |
|--------|---------|
| Anchor | ADR-001 minimal → ADR-002/003 full metadata |
| Portfolio | Full metadata from ADR-001 onward |

**Divergence:** Anchor ADRs gained governance sections over time; portfolio started with full template.

**Model implication:** Tiered decision records — not all decisions need full governance sections on day one.

---

## 9. Scope boundary sections

| Corpus | Pattern |
|--------|---------|
| Portfolio | In scope / Out of scope in every sampled ADR |
| Anchor | Present in ADR-002/003; absent in ADR-001 |

**Divergence:** Portfolio enforces scope boundary consistently; Anchor adopted it later.

**Model implication:** Scope boundary is convergent in practice, partial in historical Anchor records.

---

## Summary

Divergence is primarily in **infrastructure** and **evidence location**, not in the core decision lifecycle. A governance model can unify convergent primitives while parameterizing:

- evolution evidence layer (optional)
- meta-governance artifact type (ADR vs policy)
- relationship typing depth (by tier)
- pre-decision investigation (Tier 1 / framework only)
- bundling (allowed with structure)

No divergent pattern invalidates the hypothesis that a reusable model exists.
