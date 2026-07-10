# Extraction — Anchor releases/governance.md

**Corpus:** Anchor meta-repo  
**Artifact:** `releases/governance.md`  
**Date extracted:** 2026-07-09

## What happened?

Permanent release governance defines Evidence Window lifecycle: record observations during window, decide only at Evidence Review, separate observations from actions.

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Not a single decision — durable governance policy for post-release evolution | recording threshold |
| What evidence existed? | Pattern from framework/product validation practice | evidence source |
| What alternatives were rejected? | Not documented | — |
| How was confidence expressed? | Canonical rule stated; exit conditions enumerated; freeze table | confidence expression |
| How could this be superseded? | Implied via new governance ADR or release decision | supersession trigger |
| What governance rule is implicit? | Observe → Record → repetition → promote; two independent repos minimum | review trigger, recording threshold |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| Observations | releases/v0.2/evidence.md per release | No |
| Decisions | releases/v0.2/decision.md at review | No |
| Policy | This document | Yes |

## Primitive chain

```text
releases/governance.md
  → Governance layer separate from individual ADRs
  → Evidence source: per-release evidence.md (behavioural observations)
  → Recording during window; deciding at review only
  → Observations vs actions explicitly separated
  → Exit gate: 2+ independent repos + Evidence Review + decision.md
  → Freeze: structural changes blocked during window
```

## Notes

Framework evolution evidence system operates parallel to ADR decision records. Not embedded inside ADRs.
