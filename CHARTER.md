# Project Charter

Canonical public statement: [README.md](README.md)

## Purpose

Operational ADR packages a mature architectural decision record practice—observed across related projects during development—into an explicit model, specification, and reference implementation.

The goal is not to invent a governance theory. The goal is to capture a practice that already works and make it adoptable without access to the source repositories.

> Operational ADR was extracted from ADR practices that evolved across multiple related projects during its development. Those projects explain the specification's provenance, but they are not prerequisites for adoption. Once published, Operational ADR stands as an independent specification that any project can evaluate and adopt.

**Formerly published as Evidence-First ADR.** "Evidence-first" names the derivation methodology, not the product.

## Three distinct things

| Term | Meaning |
|------|---------|
| **The practice** | What was observed across related projects—tacit, lived (provenance in `discovery/`) |
| **The model** | Explanation of that practice—portable, explicit |
| **The specification** | How to implement the model (markdown, index, file layout) |

## Influences and provenance

**Acknowledged influences** (lineage, not competition):

- Nygard ADRs
- MADR
- Future Friendly Decision concepts

**Extraction provenance** (Phase 1 capture only):

- jon-ohio-portfolio (primary corpus)
- Anchor (secondary corpus)

See [model/traceability.md](model/traceability.md) and [discovery/](discovery/). Influences and narrative context: [analysis/comparison-v1.0.md](analysis/comparison-v1.0.md).

Portfolio and Anchor explain **why** v1.0 looks like this. They are not adoption prerequisites.

## Independence

**v1.0 shipped** (2026-07-10). The specification is independent of its origin repositories. **Operational ADR v1.0 is stable.**

| Role | Portfolio / Anchor |
|------|-------------------|
| **Historically** | Extraction sources during productization |
| **Going forward** | Anchor is one adopter among many ([validation/log.md](validation/log.md) Attempt 2); portfolio provenance job for v1.0 is complete |

Origin repos are not dependencies. Adopters need only this repository and [spec/adr-v1.0.md](spec/adr-v1.0.md).

## Methodology

> **The specification is derived from observed practice rather than designed from first principles.**

**Evidence-first** names how the specification was derived (observe → extract → model → specify)—not a requirement that every ADR embed all evidence inline. Evidence frequently lives outside the ADR; the model treats references to evidence as first-class.

## Validation question

> Can someone else adopt this practice successfully?

## Evolution principle

Operational ADR evolves through demonstrated practice and adopter feedback.

Every normative change to the practice model or specification should be traceable to one of three sources:

- validated adopter evidence (primary driver post-v1.0),
- observed adopter behaviour,
- documented shortcomings in the current specification.

Design preference alone is not sufficient justification for changing the specification.

Post-v1.0: changes are **not** justified by "the portfolio evolved, therefore the spec changes." Practices worth proposing must be validated like any other change.

## Scope

**The project owns:**

- the ADR practice model
- the ADR specification
- the reference implementation
- supporting tooling

**The project does not own:**

- Anchor
- jon-ohio-portfolio
- any specific software development methodology
- any particular repository structure

jon-ohio-portfolio and Anchor are provenance sources from Phase 1 capture—not defining authorities for adopters.

## Success

Others can adopt the practice without the author's private repositories. Broader governance-framework claims are future promotion only if validation supports them.

## Current phase

**Operational ADR v1.0 stable** (shipped 2026-07-10; renamed from Evidence-First ADR). Capture, model, spec, and reference implementation complete.

Validation ongoing: adopter feedback tracked in [validation/log.md](validation/log.md). Resist feature work until adoption evidence warrants it.

## v1.1 gate

Version 1.1 opens when evidence arrives from:

- independent adopters,
- migration experiences (Nygard, MADR, custom templates),
- documented friction or shortcomings in the current specification.

Not from feature ideas alone. Not from origin repository changes alone.

The model and spec change only if validated adopter evidence, adopter behaviour, or documented shortcomings contradict them.
