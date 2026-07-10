# Extraction — Portfolio ADR-073

**Corpus:** jon-ohio-portfolio  
**Artifact:** `docs/adrs/ADR-073-case-study-progress-status-dark-default-homepage-headline.md`  
**Date extracted:** 2026-07-09

## What happened?

Single ADR bundled three UX decisions: WIP badge, dark theme default, homepage headline — shipped together on one branch (PRs #178–#179).

## Extraction

| Question | Observation | Suggested primitive |
|----------|-------------|---------------------|
| What triggered this decision? | Three related UX gaps shipped together on branch cursor/wip-badge-95593 | recording threshold |
| What evidence existed? | PR references; prior ADR-070 theme behaviour; product direction shift | evidence source |
| What alternatives were rejected? | Multiple option sets (A–E) per sub-decision with reject notes | rejected alternatives preserved |
| How was confidence expressed? | Accepted; risks per sub-decision; Review Schedule 2026-12-29 | confidence expression |
| How could this be superseded? | Per-sub-decision rollback paths in Operational Impact; narrows ADR-070 | supersession trigger |
| What governance rule is implicit? | Related ADRs graph (002, 007, 070, 036, 072); amends ADR-070 default behaviour | scope boundary |

## Evidence location

| Evidence type | Where it lives | Inside artifact? |
|---------------|----------------|------------------|
| PR evidence | References #178, #179 | No (link) |
| Prior ADRs | Related ADRs section (5 links) | No |
| Sub-decision options | Options A–E in body | Yes |

## Primitive chain

```text
ADR-073
  → Recording threshold: bundled ship on single branch
  → Multiple decisions in one ADR (status + theme + headline)
  → Each sub-decision has own options and chosen path
  → Narrows/supersedes aspect of ADR-070 (time-of-day fallback)
  → Rich Related ADRs graph with relationship verbs (constrains, narrows)
```

## Notes

Demonstrates bundling related decisions. Relationship types more explicit than Anchor ADRs.
