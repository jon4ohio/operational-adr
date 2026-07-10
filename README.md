# Operational ADR

A compatible ADR implementation distilled from long-term **operational** practice. It remains compatible with established ADR approaches (Nygard, MADR) while adding optional capabilities that have proven useful in managing architectural decisions over time.

**Operational ADR was originally published as Evidence-First ADR.** The rename reflects a clarification of identity: "evidence-first" describes the methodology used to derive the implementation, not the purpose of the implementation itself.

**Maintainer recommendation** — not a claim of universal superiority.

**Methodology note:** This specification was derived from observed practice (evidence-first productization). That describes how it was built, not what an ADR is for. ADRs record significant project decisions.

Tag `v1.0.0` was published under the former name; the content is the same practice.

---

## What it is

**Operational ADR is a portable Architectural Decision Record practice.**

It was extracted from ADR practices that evolved across multiple related projects during its development, influenced by established approaches such as Nygard ADRs, MADR, and Future Friendly Decision concepts. Provenance is documented in [`discovery/`](discovery/).

**Those origin projects explain why the specification looks the way it does—but they are not prerequisites for adoption.** Once published, Operational ADR stands as an independent specification that any project can evaluate and adopt.

The project does not attempt to replace existing ADR approaches or introduce a universal decision governance framework.

Instead, it documents, packages, and publishes a mature way of working so that other teams can adopt, adapt, and evaluate it independently.

---

## Why it exists

Over time, the portfolio and Anchor developed a consistent way of working with Architectural Decision Records.

That practice was never written down as a reusable system.

It existed as:

- conventions,
- document structure,
- relationships,
- supersession,
- review,
- supporting artifacts,
- and accumulated experience.

Operational ADR exists to capture that practice before it remains only tacit knowledge.

Origin capture is complete. **Adopters start at [spec/adr-v1.0.md](spec/adr-v1.0.md)**—not at the portfolio or Anchor repositories.

---

## How it was created

Unlike many specifications that begin from design discussions or first principles, Operational ADR was built by productizing an existing practice.

```text
Existing ADR Practice
        │
        ▼
Capture
        │
        ▼
Practice Model
        │
        ▼
Specification
        │
        ▼
Reference Implementation
        │
        ▼
Validation
```

The capture work is complete.

The specification is derived from observed practice rather than invented independently. See [model/traceability.md](model/traceability.md) for provenance.

**Evidence-first** names this derivation methodology—not a requirement that every ADR embed all evidence inline. Evidence often lives in PRs, logs, experiments, and indexes; the ADR references it.

---

## Origin and adoption

Two stories apply to different audiences. Do not confuse them.

### Origin (historical — author and researchers)

How this project was built. Portfolio and Anchor are relatable here because the same maintainer evolved practice across both—they are **provenance**, not adoption prerequisites.

```text
Existing practice
(across related projects during development)
        │
        ▼
Capture (discovery/)
        │
        ▼
Operational ADR v1.0
(published as Evidence-First ADR)
```

### Adoption (everyone else)

How to use the published specification. Anchor is **one adopter among many**—it shares history with the project but that history is not required for anyone else.

```text
Operational ADR
        │
        ├── Project A
        ├── Project B
        ├── Project C
        └── Anchor (one adopter)
```

### Independence milestone

v1.0 publish means the **specification is independent of its origin**. The portfolio's role as provenance source for v1.0 is complete. Future spec changes are not justified by "the portfolio evolved, therefore the spec changes"—they require validated proposals from adopters, like any other project.

---

## Project architecture

```text
discovery/
    Capture of existing practice
    (research appendix)

        │

        ▼

model/
    ADR Practice Model
    Traceability
    Relationships
    Lifecycle

        │

        ▼

spec/
    ADR Specification

        │

        ▼

decisions/
    Reference implementation

        │

        ▼

validation/
    Adoption evidence
```

Each layer has a distinct responsibility.

| Layer | Responsibility |
|-------|----------------|
| **Discovery** | Provenance archive—why v1.0 looks like this (not required for adoption) |
| **Model** | Explains the practice |
| **Specification** | Explains how to implement it |
| **Reference implementation** | Demonstrates it |
| **Validation** | Determines how it evolves |

Governance detail: [CHARTER.md](CHARTER.md)

---

## What makes it different

The value of the project is not that it invents new ADR concepts.

**Influences** (ideas the practice draws on):

- Nygard
- MADR
- Future Friendly Decision

**Provenance** (extraction corpus—why the v1.0 spec looks like this):

- jon-ohio-portfolio and Anchor — documented in [`discovery/`](discovery/), not an adoption path

The contribution is bringing influences and observed practice together into one coherent, documented specification.

More importantly, every significant part of the specification can be traced back to observed practice.

The project doesn't simply state:

> "This is the specification."

It can also answer:

> "This is why the specification looks like this."

Peer comparison: [analysis/comparison-v1.0.md](analysis/comparison-v1.0.md)

---

## Evolution principle

Operational ADR evolves through demonstrated practice and adopter feedback.

Every normative change to the practice model or specification should be traceable to one of three sources:

- validated adopter evidence (primary driver post-v1.0),
- observed adopter behaviour,
- documented shortcomings in the current specification.

Design preference alone is not sufficient justification for changing the specification.

Post-v1.0 changes are **not** justified by "the portfolio evolved, therefore the spec changes." A practice worth proposing must be validated like any other change—from adopters, migration friction, or documented spec gaps.

Full governance: [CHARTER.md](CHARTER.md)

---

## Version 1.0

Version 1.0 represents the successful productization of an existing ADR practice. **Operational ADR v1.0 is stable** — use it, recommend it, observe it. Do not treat this rename as the start of feature work.

It includes:

- ADR Practice Model — [model/adr-practice-model-v1.0.md](model/adr-practice-model-v1.0.md)
- Traceability — [model/traceability.md](model/traceability.md)
- ADR Specification — [spec/adr-v1.0.md](spec/adr-v1.0.md)
- Reference Implementation — [decisions/](decisions/)
- Validation log — [validation/log.md](validation/log.md)
- Comparative analysis — [analysis/comparison-v1.0.md](analysis/comparison-v1.0.md)

The objective of Version 1.0 is not to prove that the practice is superior to Nygard or MADR.

Its objective is much simpler:

> **Can another team adopt this ADR practice without needing the projects from which it evolved?**

---

## Version 1.1 and beyond

Future versions should be driven by adoption rather than feature development.

Evidence should come from:

- independent adopters,
- migration experiences,
- observed friction,
- implementation feedback.

The project should resist adding features simply because they seem useful.

Instead, it should continue the same philosophy that produced Version 1.0:

> Capture practice.
>
> Explain practice.
>
> Package practice.
>
> Validate practice.
>
> Improve practice through evidence.

---

## Quick start

1. Read [spec/adr-v1.0.md](spec/adr-v1.0.md)
2. Create `decisions/` in your project
3. Write your first ADR at Tier 0 or Tier 1
4. Add `index.md` when you reach ~10 ADRs

---

## Documents

| Document | Role |
|----------|------|
| [CHARTER.md](CHARTER.md) | Operational governance and scope |
| [model/traceability.md](model/traceability.md) | Provenance: extractions → model elements |
| [model/adr-practice-model-v1.0.md](model/adr-practice-model-v1.0.md) | Explanation of the practice |
| [spec/adr-v1.0.md](spec/adr-v1.0.md) | Markdown serialization of the model |
| [decisions/](decisions/) | Reference implementation |
| [discovery/](discovery/) | Provenance archive (research—not required for adoption) |
| [validation/log.md](validation/log.md) | Adoption evidence |
| [analysis/comparison-v1.0.md](analysis/comparison-v1.0.md) | Peer comparison (Nygard, MADR) |

---

## License

Documentation, specifications, and templates in this repository are licensed under [CC BY 4.0](LICENSES/CC-BY-4.0.md).

Software contained in this repository is licensed under [MIT](LICENSES/MIT.md).
