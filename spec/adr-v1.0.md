# ADR Specification v1.0

**Status:** Phase 3 — markdown serialization of [ADR Practice Model v1.0](../model/adr-practice-model-v1.0.md)  
**Date:** 2026-07-10  
**Derived from:** Observed practice, not first principles. See [traceability.md](../model/traceability.md).

This specification defines how to implement the ADR practice model as markdown files in a repository.

---

## 1. File layout

```text
decisions/
  ADR-NNN-short-title.md    # Individual decision records
  index.md                  # Tabular index (recommended at 10+ ADRs)
  LOG.md                    # Optional chronological audit
```

**Naming:** `ADR-NNN-short-title.md` where NNN is zero-padded sequential number (001, 002, …) and short-title is kebab-case slug.

**Location:** `decisions/` at repository root, or `docs/decisions/` / `docs/adrs/` if project convention requires—document the choice in README or meta-governance.

---

## 2. ADR document structure

### Tier 0 — Minimal (required sections)

Every ADR MUST include:

```markdown
# ADR-NNN: [Short Descriptive Title]

## Status
**Status:** [Draft | Proposed | Accepted | Deprecated | Superseded by ADR-NNN]
**Date:** [YYYY-MM-DD]
**Decision Maker(s):** [names or roles]
**Supersedes:** [ADR-NNN or None]

## Context
[Why this decision is needed now.]

## Decision
[What was decided.]

## Consequences
### Positive
- [Outcome]

### Negative / Trade-offs
- [Trade-off]
```

### Tier 1 — Full (recommended sections)

Tier 1 ADRs SHOULD include all Tier 0 sections plus:

```markdown
## Decision Drivers
- [Driver — specific and testable]

## Options Considered

### Option A: [Name]
- **Description:** [summary]
- **Pros:** [list]
- **Cons:** [list — at least one required]
- **Effort:** [Low | Medium | High]

### Option B: [Name]
...

## Context (extended)
**In scope:** [what this ADR governs]
**Out of scope:** [what is explicitly excluded]

## Consequences (extended)
### Operational Impact
- [Effect on onboarding, maintenance, observability]
- **Migration / rollback:** [steps; how to revert]

### Risks

| Risk | Likelihood | Impact | Mitigation | Owner/Role | Review Trigger |
|------|-----------|--------|------------|------------|----------------|
| [Risk] | Low/Med/High | Low/Med/High | [Mitigation] | [Owner] | [Trigger] |

## Review Schedule
- **Next review:** [date or trigger event]
- **Review owner:** [name or role]

## Related ADRs
- [ADR-NNN — relationship: depends on / supersedes / constrains / amends / follow-up]

## References
- [Primary source: docs, PRs, prior ADRs]
```

**Relationship verbs (portfolio convention):** `depends on`, `supersedes`, `constrains`, `amends`, `follow-up`. Informal lists acceptable at Tier 0.

---

## 3. Status values

| Status | Meaning |
|--------|---------|
| Draft | Work in progress; not binding |
| Proposed | Ready for review; not yet accepted |
| Accepted | Binding; immutable except non-substantive corrections |
| Deprecated | No longer recommended; not superseded by specific ADR |
| Superseded by ADR-NNN | Replaced; see named ADR |

When status is Superseded, update the superseding ADR's `Supersedes` field and the index `Superseded By` column.

---

## 4. Immutability and supersession

1. Do not edit substance of Accepted ADRs.
2. To change a decision, create a new ADR with `Supersedes: ADR-NNN`.
3. Update the old ADR's status to `Superseded by ADR-NNN` (status line only—no other edits).
4. Update `index.md` Superseded By column.
5. Optionally append to `LOG.md`.

Non-substantive corrections (typos, broken links) are permitted when explicitly requested and confirmed—no semantic change.

---

## 5. Recording threshold (meta-governance)

Document when ADRs are required. Choose one:

**Option A — ADR (portfolio style):** A meta-governance ADR (e.g., ADR-008) defines triggers: major pushes affecting architecture, tokens, routing, data model, or workflow.

**Option B — Policy doc (Anchor style):** CONTRIBUTING or similar states: write an ADR when a decision "constrains future work."

Both satisfy the model. This specification does not mandate which.

---

## 6. Index format

`decisions/index.md` — tabular lookup:

```markdown
# ADR Index

| ADR | Title | Status | Date | Superseded By |
|-----|-------|--------|------|---------------|
| [ADR-001](ADR-001-short-title.md) | Short Title | Accepted | YYYY-MM-DD | — |
| [ADR-002](ADR-002-other.md) | Other | Superseded | YYYY-MM-DD | ADR-003 |
```

Recommended when decision count exceeds ~10 or supersession chains appear.

---

## 7. LOG format (optional)

`decisions/LOG.md` — chronological acceptance audit:

```markdown
# ADR Log

| Date | ADR | Event | Notes |
|------|-----|-------|-------|
| YYYY-MM-DD | ADR-001 | Accepted | Initial convention |
```

---

## 8. Evidence references

ADRs SHOULD reference external evidence in Context, References, or Operational Impact. Evidence may live in:

- Pull requests and commit history
- Experiment logs or release evidence files
- Design conversations (linked or summarized)
- Prior ADRs

This specification does **not** require inline evidence tables inside ADRs. Pre-decision evidence tables (Anchor coordination-problem template) are an optional Tier 2 extension for high-stakes or framework-level decisions.

---

## 9. Tier selection guide

| Situation | Recommended tier |
|-----------|------------------|
| New project, &lt;5 ADRs | Tier 0 |
| Product repo, 10+ ADRs, supersession chains | Tier 1 + index |
| Long-lived codebase with governance review | Tier 1 + index + LOG |
| Framework with pre-promotion investigation | Tier 2 extensions |

Early ADRs may be Tier 0; later ADRs may adopt Tier 1 as practice matures (Anchor maturity curve).

---

## 10. Anchor variant (documented subset)

Anchor projects MAY use Tier 0 only, with:

- Evolution evidence in `releases/evidence.md` (separate from ADRs)
- POSITION papers for gated promotion before ADR
- coordination-problem template for pre-decision investigation
- Informal Related ADRs until scale demands typed verbs

See [model §11 Variants](../model/adr-practice-model-v1.0.md#11-variants).

---

## 11. Validation checklist

An implementation conforms to this spec if:

- [ ] ADRs live in a documented directory with `ADR-NNN-short-title.md` naming
- [ ] Tier 0 sections present in every ADR
- [ ] Accepted ADRs are not substantively edited in place
- [ ] Supersession creates new ADR and updates status/index
- [ ] Recording threshold documented (ADR or policy)
- [ ] Index present when 10+ ADRs or supersession chains exist

---

## 12. Related documents

| Document | Role |
|----------|------|
| [adr-practice-model-v1.0.md](../model/adr-practice-model-v1.0.md) | Conceptual model this spec implements |
| [traceability.md](../model/traceability.md) | Provenance |
| [decisions/](../decisions/) | Reference implementation |
