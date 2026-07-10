# Extraction — Anchor coordination-problem TEMPLATE

**Corpus:** Anchor meta-repo  
**Artifact:** `research/coordination-problem/TEMPLATE.md`  
**Date extracted:** 2026-07-09

## What happened?

Template for coordination-problem investigations: hypothesis, observation types, evidence table, falsification attempts, binary outcome.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Recurring coordination failures may justify new capabilities — investigated before building | recording threshold |
| What evidence existed? | Evidence table: Observation, Evidence link, Recurs?, Existing practice solved it? | evidence source |
| What alternatives were rejected? | Falsification attempts section — seek counter-evidence | rejected alternatives preserved |
| How was confidence expressed? | Outcome: Open / Yes / No; insufficient evidence keeps Open | confidence expression |
| How could this be superseded? | Investigation closes Supported or Not supported; Phase 2 only if Supported | supersession trigger |
| What governance rule is implicit? | Do not invent features; capabilities emerge from observed failures | recording threshold |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Session references | Evidence table rows | Partially |
| Counter-evidence | Falsification attempts table | Yes |
| Outcome | Outcome section | Yes |

## Primitive chain

```text
coordination-problem/TEMPLATE
  → Pre-capability investigation (not ADR)
  → Evidence table with recurrence and falsification columns
  → Falsification discipline: try to disprove hypothesis
  → Binary outcome gate before implementation
  → Status remains Open until sufficient evidence
```

## Notes

Strongest evidence-first pattern in Anchor corpus. Governs framework capability emergence, not individual architectural decisions.
