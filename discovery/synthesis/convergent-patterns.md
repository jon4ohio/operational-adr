# Convergent Patterns

**Status:** Discovery Phase 1 synthesis  
**Date:** 2026-07-09

Patterns observed in **both** Anchor and jon-ohio-portfolio corpora.

---

## 1. Record when future work is constrained

**Anchor:** CONTRIBUTING — ADR when decision "constrains future work." ADR-001 freezes when design questions become empirical.

**Portfolio:** ADR-008 — major pushes affecting architecture, tokens, routing, data model, or workflow require ADR action.

**Convergent rule (observed):** Durable records appear when reversal cost or traceability demand exceeds informal memory.

---

## 2. Immutability with supersession

**Anchor:** "ADRs are immutable once accepted. To change a decision, supersede with a new ADR." (CONTRIBUTING, ADR-001 Operational Impact)

**Portfolio:** ADR-025 status → Superseded by ADR-026. Index `Superseded By` column. ADR-079 supersedes ADR-041 in effect without editing ADR-041.

**Convergent rule (observed):** Decisions are not edited in place. New record replaces old; chain preserved.

---

## 3. Alternatives are project knowledge

**Anchor:** ADR-001 (four options), ADR-002 (three options), ADR-003 (three options) — all with pros/cons.

**Portfolio:** Every sampled ADR includes Options Considered with rejected paths documented.

**Convergent rule (observed):** Rejected options remain readable. Rationale for rejection is preserved.

---

## 4. Confidence through status and risks

**Anchor:** Accepted status + risks table (likelihood, impact, mitigation, owner, review trigger) from ADR-001 onward.

**Portfolio:** Same risks table pattern from ADR-001 onward. ADR-069 adds explicit success criteria.

**Convergent rule (observed):** Acceptance is not bare assertion. Risks and owners make confidence auditable.

---

## 5. Scheduled review

**Anchor:** ADR-002 review after portfolio/greenfield validation. ADR-003 review after v0.2 Evidence Review.

**Portfolio:** ADR-001, 008, 069, 073, 079 all include Review Schedule with date or event trigger.

**Convergent rule (observed):** Decisions carry expiry or revisit conditions — not permanent silent acceptance.

---

## 6. Named decision ownership

**Anchor:** Decision Maker(s) in metadata — Project maintainer.

**Portfolio:** Decision Maker(s) — John Ohio / Jon Ohio (Owner/Maintainer / Product Design Lead).

**Convergent rule (observed):** Every durable decision has a named owner, not anonymous consensus.

---

## 7. Evidence often lives outside the decision record

**Anchor:** Design conversations (ADR-001), experiment logs (POSITION), release evidence.md (governance.md).

**Portfolio:** PR references (ADR-073), commit history (ADR-026), decision log (ADR-008 chain).

**Convergent rule (observed):** The ADR summarizes and points; raw evidence frequently external. Neither corpus embeds formal pre-decision evidence tables inside ADRs.

---

## Implication for Governance Model v1.0

The convergent core is a **decision lifecycle**:

```text
Trigger (threshold met)
  → Evidence gathered (often external)
  → Alternatives evaluated and preserved
  → Decision recorded with owner, status, risks
  → Review scheduled
  → Supersession path defined
  → Immutability enforced
```

This lifecycle is independent of markdown, Anchor, or portfolio structure.
