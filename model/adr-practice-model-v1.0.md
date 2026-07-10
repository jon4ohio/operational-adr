# ADR Practice Model v1.0

**Status:** Phase 2 — explanation of existing practice  
**Date:** 2026-07-10  
**Provenance:** Every section maps to [traceability.md](traceability.md)

This document explains the ADR practice observed across long-running software projects. It makes existing relationships explicit—it does not introduce a new semantic theory.

---

## 1. Purpose

An Architectural Decision Record (ADR) is a durable record of a significant technical or architectural choice: what was decided, why, what was rejected, and how the decision may change.

The practice exists because informal memory fails at scale. When reversal cost or traceability demand exceeds what chat, PR descriptions, or contributor habit can sustain, a durable record is written.

---

## 2. When to write an ADR (recording threshold)

Write an ADR when a decision **constrains future work**—when reversing or forgetting it would cost more than maintaining a record.

**Observed triggers (both corpora):**

| Trigger | Source |
|---------|--------|
| Recurring architectural tension | Anchor ADR-002 |
| Design questions become empirical (freeze and validate) | Anchor ADR-001 |
| Adoption or validation friction | Anchor ADR-003 |
| Major push affecting architecture, tokens, routing, data model, or workflow | Portfolio ADR-008 |
| IA or structural change that triggers meta-governance | Portfolio ADR-079 |
| Codify existing convention before drift | Portfolio ADR-001 |
| Capability demonstrated; identity-level claim needs durable record | Anchor POSITION |

**Meta-governance:** The recording threshold itself may be documented as an ADR (portfolio ADR-008) or contributor policy (Anchor CONTRIBUTING). Both are valid.

---

## 3. Decision lifecycle

The convergent lifecycle observed in both corpora:

```text
Threshold met
  → Evidence gathered (often external)
  → Alternatives evaluated and preserved
  → Decision recorded with owner, status, risks
  → Review scheduled
  → Supersession path defined
  → Immutability enforced
```

**Provenance:** [convergent-patterns.md](../discovery/synthesis/convergent-patterns.md), all 16 extractions.

### 3.1 Evidence gathered

Evidence frequently lives **outside** the ADR. The ADR summarizes and points; raw material may be in PRs, commit history, experiment logs, release evidence windows, or design conversations.

See [evidence-location-map](../discovery/synthesis/evidence-location-map.md). Neither corpus mandates inline evidence tables inside ADRs.

### 3.2 Alternatives evaluated and preserved

Rejected options remain documented with rationale. Options Considered sections include pros, cons, and effort where observed.

**Provenance:** All ADR extractions in both corpora.

### 3.3 Decision recorded

Minimum durable content: Context, Decision, Consequences. Mature records add Decision Drivers, Options Considered, Risks, Review Schedule, Related ADRs.

### 3.4 Review scheduled

Decisions carry expiry or revisit conditions—not permanent silent acceptance. Review may be date-based or event-triggered (e.g., after validation, after case study publish).

**Provenance:** Anchor ADR-002/003; portfolio ADR-001, 008, 069, 073, 079.

### 3.5 Supersession path defined

Accepted ADRs are immutable. To change a decision, create a new ADR that supersedes the old one. The supersession chain is preserved—not edited in place.

**Provenance:** Anchor CONTRIBUTING, ADR-001; portfolio ADR-025→026, ADR-079, index.

### 3.6 Immutability enforced

Do not edit substance of Accepted ADRs. Non-substantive corrections (typos, broken links) are allowed when explicitly requested and confirmed.

---

## 4. Confidence expression

Acceptance is not bare assertion. Confidence is communicated through:

| Mechanism | Observed in |
|-----------|-------------|
| Status (Draft, Proposed, Accepted, Deprecated, Superseded) | Both corpora |
| Risks table (likelihood, impact, mitigation, owner, review trigger) | Both corpora from early ADRs |
| Decision Drivers | Anchor ADR-002+; portfolio ADR-001+ |
| Success criteria in Decision body | Portfolio ADR-069 |
| Review Schedule | Both corpora |

---

## 5. Decision ownership

Every durable decision has a named owner in metadata (`Decision Maker(s)`). Not anonymous consensus.

**Provenance:** All sampled ADRs in both corpora.

---

## 6. Scope boundary

Explicit **In scope** and **Out of scope** sections limit what the decision governs. Portfolio enforces this consistently; Anchor adopted it in later ADRs.

**Provenance:** Portfolio all samples; Anchor ADR-002/003.

---

## 7. Relationships between decisions

Decisions link to other decisions. Portfolio makes implicit semantics explicit with typed verbs:

| Relationship | Meaning (observed) |
|--------------|-------------------|
| depends on | This decision assumes another |
| supersedes | This decision replaces another in effect |
| constrains | This decision limits options in another |
| amends | This decision modifies interpretation without full supersession |

Anchor uses informal Related ADRs lists. At scale, typed relationships and stale-rationale notes (portfolio ADR-079) reduce lookup cost.

**Model treatment:** Relationship typing is a **tier parameter**—recommended at scale, not required for every project.

---

## 8. Evidence ecosystem

The ADR is one artifact in a larger evidence ecosystem:

| Artifact | Role | Corpus |
|----------|------|--------|
| ADR | Durable decision summary + pointers | Both |
| Index | Lookup by status, Superseded By | Portfolio |
| LOG | Chronological acceptance audit | Portfolio |
| Release evidence window | Project evolution governance | Anchor |
| POSITION paper | Gated promotion before ADR | Anchor |
| coordination-problem template | Pre-decision investigation | Anchor |
| PRs, commits | Implementation verification | Portfolio |

**Key principle:** References to evidence are first-class. The model does not mandate stuffing evidence into the ADR body.

---

## 9. Supporting infrastructure

### 9.1 Decision index

Tabular index of all ADRs: number, title, status, date, superseded-by. Essential at 20+ records.

**Provenance:** [portfolio/index extraction](../discovery/extraction/portfolio/index-extraction.md)

### 9.2 Decision log (LOG)

Chronological audit of ADR acceptance events. Optional but valuable for governance review.

**Provenance:** [portfolio/LOG extraction](../discovery/extraction/portfolio/LOG-extraction.md)

### 9.3 Meta-governance record

Defines when ADRs are required. May be ADR (portfolio) or policy doc (Anchor).

---

## 10. Tiers

The practice supports tiered adoption—not every decision needs full governance sections on day one.

### Tier 0 — Minimal (Anchor lean contract)

- Context, Decision, Consequences
- Options Considered (when alternatives exist)
- Status, Date, Decision Maker(s)
- Related ADRs (informal)

Suitable for early project ADRs or framework repos with low decision count.

**Provenance:** Anchor ADR-001; Anchor CONTRIBUTING contract.

### Tier 1 — Full (portfolio rich template)

Everything in Tier 0, plus:

- Decision Drivers
- In scope / Out of scope
- Risks table with owner and review trigger
- Review Schedule
- Typed Related ADRs (depends on, supersedes, constrains, amends)
- References (primary sources, PRs, prior ADRs)

Suitable for product repos, long-lived codebases, or 10+ ADRs.

**Provenance:** Portfolio ADR-001 onward; Anchor ADR-002/003 maturity curve.

### Tier 2 — Infrastructure (optional extensions)

- Decision index with Superseded By column
- LOG.md chronological audit
- Pre-decision investigation (coordination-problem template)
- Gated promotion artifacts (POSITION papers)
- Release evidence windows

**Provenance:** [divergent-patterns.md](../discovery/synthesis/divergent-patterns.md)

---

## 11. Variants

### Portfolio variant (primary)

Rich template from ADR-001. Index + LOG at scale. Meta-governance as ADR-008. Typed relationships and stale-rationale marking.

### Anchor variant (documented subset)

Lean ADR contract in CONTRIBUTING. Evolution evidence in `releases/evidence.md` separate from ADRs. POSITION papers and coordination-problem template for pre-promotion investigation. Informal Related ADRs until scale demands typing.

Both variants share the same lifecycle and convergent primitives. They differ in infrastructure depth and meta-governance artifact choice.

---

## 12. Optional patterns

| Pattern | When | Provenance |
|---------|------|------------|
| Decision bundling | Related decisions shipped in one PR/branch | Portfolio ADR-073 |
| Stale rationale marking | Prior ADR rationale outdated but record immutable | Portfolio ADR-079 |
| Success criteria in Decision | Outcome must be verifiable | Portfolio ADR-069 |
| Governance metadata maturity curve | Early ADRs minimal; later ADRs full | Anchor ADR-001 → 002/003 |

---

## 13. What v1.0 does not specify

- Cardinality rules (how many options, risks, or relationships)
- Mandatory inline evidence tables
- Universal governance framework claims
- Comparison with Nygard/MADR as normative (peer comparison is optional validation)

Model and spec change only if capture evidence contradicts them—not because external formats suggest retrofitting.

---

## 14. Related documents

| Document | Relationship |
|----------|--------------|
| [traceability.md](traceability.md) | Provenance for every model element |
| [spec/adr-v1.0.md](../spec/adr-v1.0.md) | Markdown serialization of this model |
| [discovery/synthesis/governance-primitives.md](../discovery/synthesis/governance-primitives.md) | Primitive catalog from capture |
| [discovery/synthesis/convergent-patterns.md](../discovery/synthesis/convergent-patterns.md) | Cross-corpus convergence |
