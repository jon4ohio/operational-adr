# Capture — Existing ADR Practice

Phase 1 captured recurring patterns from two long-running projects. This is **not** research into whether a practice exists—the practice was already in use. Capture makes tacit knowledge explicit before it is lost.

## Corpus sources

| Corpus | Path | Role |
|--------|------|------|
| jon-ohio-portfolio | `../../Portfolio/jon-ohio-portfolio/` | Primary source (80+ ADRs, index, LOG) |
| Anchor meta-repo | `../../agentic workflow/` | Secondary source (lean contract, ecosystem patterns) |

## Operating rules (capture phase)

1. **Descriptive only** — What happened? What was observed? What primitive does it suggest?
2. **Convergence in synthesis** — One occurrence is observation; repetition across corpora is evidence.
3. **Traceability** — Every model element must map back to extractions in [model/traceability.md](../model/traceability.md).
4. **Comparison does not rewrite capture** — Nygard/MADR comparison comes after the model is written.

## Milestone 1 — Capture complete

**Deliverables:**

- 16 extractions in `extraction/anchor/` and `extraction/portfolio/`
- Synthesis in `synthesis/` (governance-primitives, convergent/divergent patterns, evidence-location map)

**v1.0 shipped (2026-07-10).** Productization complete. Start with [README.md](../README.md); adopt via [spec/adr-v1.0.md](../spec/adr-v1.0.md). This folder remains the research appendix.
