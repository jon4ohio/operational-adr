# Project Charter

Canonical public statement: [README.md](README.md)

## Purpose

Evidence-First ADR packages a mature architectural decision record practice—refined through long-term use across multiple software projects—into an explicit model, specification, and reference implementation.

The goal is not to invent a governance theory. The goal is to capture a practice that already works and make it adoptable without access to the source repositories.

## Three distinct things

| Term | Meaning |
|------|---------|
| **The practice** | What has been done for years (portfolio, Anchor)—tacit, lived |
| **The model** | Explanation of that practice—portable, explicit |
| **The specification** | How to implement the model (markdown, index, file layout) |

## Influences

Lineage, not competition:

- Nygard ADRs
- MADR
- Future Friendly Decision concepts
- jon-ohio-portfolio practice (primary corpus)
- Anchor refinements (secondary corpus)

Phase 1 extraction provenance covers portfolio and Anchor only. See [model/traceability.md](model/traceability.md). Other influences are acknowledged in narrative and [analysis/comparison-v1.0.md](analysis/comparison-v1.0.md).

## Methodology

> **The specification is derived from observed practice rather than designed from first principles.**

**Evidence-first** names how the specification was derived (observe → extract → model → specify)—not a requirement that every ADR embed all evidence inline. Evidence frequently lives outside the ADR; the model treats references to evidence as first-class.

## Validation question

> Can someone else adopt this practice successfully?

## Evolution principle

Evidence-First ADR evolves through demonstrated practice and adopter feedback.

Every normative change to the practice model or specification should be traceable to one of three sources:

- established practice,
- observed adopter behaviour,
- documented shortcomings in the current specification.

Design preference alone is not sufficient justification for changing the specification.

## Scope

**The project owns:**

- the ADR practice model
- the ADR specification
- the reference implementation
- supporting tooling

**The project does not own:**

- Anchor
- any specific software development methodology
- any particular repository structure

jon-ohio-portfolio and Anchor are sources of captured practice, not defining authorities.

## Success

Others can adopt the practice without the author's private repositories. Broader governance-framework claims are future promotion only if validation supports them.

## Current phase

**v1.0 shipped** (2026-07-10). Capture, model, spec, and reference implementation complete.

Validation ongoing: external adopter feedback tracked in [validation/log.md](validation/log.md).

## v1.1 gate

Version 1.1 opens when evidence arrives from:

- independent adopters,
- migration experiences (Nygard, MADR, custom templates),
- documented friction or shortcomings in the current specification.

Not from feature ideas alone.

The model and spec change only if capture evidence, adopter behaviour, or documented shortcomings contradict them.
