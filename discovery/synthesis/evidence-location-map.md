# Evidence Location Map

**Status:** Discovery Phase 1 synthesis  
**Date:** 2026-07-09

Where evidence lives relative to decision records in each corpus.

---

## Anchor meta-repo

| Evidence type | Primary location | Inside ADR? | Example |
|---------------|------------------|-------------|---------|
| Design discussion | Context narrative, References | Partially | ADR-001 |
| Adoption validation | Context narrative | Partially | ADR-003 |
| Experiment results | `releases/v0.2/context-arbitration-experiment.md` | No | POSITION paper |
| Release observations | `releases/v0.2/evidence.md` | No | governance.md |
| Framework change friction | `ai/handoff.md` friction log | No | CONTRIBUTING |
| Capability investigation | `research/coordination-problem/*.md` | No | TEMPLATE |
| Competing options | Options Considered section | Yes | All ADRs |
| Risk assessment | Risks table in ADR | Yes | ADR-001+ |

---

## jon-ohio-portfolio

| Evidence type | Primary location | Inside ADR? | Example |
|---------------|------------------|-------------|---------|
| Repo convention | Context + CLAUDE.md | Partially | ADR-001 |
| PR / branch work | References section | No | ADR-073 (#178, #179) |
| Commit history | Risk mitigation note | No | ADR-026 |
| Prior ADR chain | Related ADRs links | No | ADR-026 → ADR-025 |
| Competing options | Options Considered | Yes | All ADRs |
| Supersession state | `index.md` Superseded By | No | ADR-025 → 026 |
| Acceptance chronology | `LOG.md` | No | All acceptances |
| Risk assessment | Risks table in ADR | Yes | All sampled |

---

## Cross-corpus observation

Neither corpus embeds structured pre-decision evidence tables **inside** individual ADRs. Evidence is:

1. Narrative in Context
2. Linked external artifacts (PRs, experiments, logs)
3. Preserved in rejected Options

Anchor additionally maintains **parallel evidence systems** for framework evolution (evidence.md, coordination-problem investigations) that never appear inside ADRs.

**Implication:** A governance model that mandates in-ADR evidence tables would be **novel** relative to observed practice — not a extraction of existing behaviour. Any Evidence section in the specification must be justified as governance improvement, not as documentation of current practice.
