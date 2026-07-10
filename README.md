# Evidence-First ADR

## What it is

**Evidence-First ADR is a portable Architectural Decision Record practice.**

It captures an ADR practice that evolved during the development of substantial software projects, influenced by established approaches such as Nygard ADRs, MADR, and Future Friendly Decision concepts, and refined through practical use across the jon-ohio-portfolio and Anchor projects.

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

Evidence-First ADR exists to capture that practice before it remains only tacit knowledge.

---

## How it was created

Unlike many specifications that begin from design discussions or first principles, Evidence-First ADR was built by productizing an existing practice.

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
| **Discovery** | Explains where the practice came from |
| **Model** | Explains the practice |
| **Specification** | Explains how to implement it |
| **Reference implementation** | Demonstrates it |
| **Validation** | Determines how it evolves |

Governance detail: [CHARTER.md](CHARTER.md)

---

## What makes it different

The value of the project is not that it invents new ADR concepts.

Most ideas have clear lineage:

- Nygard
- MADR
- Future Friendly Decision
- long-term portfolio practice
- refinements explored through Anchor

The contribution is bringing those influences together into one coherent, documented practice.

More importantly, every significant part of the specification can be traced back to observed practice.

The project doesn't simply state:

> "This is the specification."

It can also answer:

> "This is why the specification looks like this."

Peer comparison: [analysis/comparison-v1.0.md](analysis/comparison-v1.0.md)

---

## Evolution principle

Evidence-First ADR evolves through demonstrated practice and adopter feedback.

Every normative change to the practice model or specification should be traceable to one of three sources:

- established practice,
- observed adopter behaviour,
- documented shortcomings in the current specification.

Design preference alone is not sufficient justification for changing the specification.

Full governance: [CHARTER.md](CHARTER.md)

---

## Version 1.0

Version 1.0 represents the successful productization of an existing ADR practice.

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
| [discovery/](discovery/) | Phase 1 capture (research appendix) |
| [validation/log.md](validation/log.md) | Adoption evidence |
| [analysis/comparison-v1.0.md](analysis/comparison-v1.0.md) | Peer comparison (Nygard, MADR) |

---

## License

Documentation, specifications, and templates in this repository are licensed under [CC BY 4.0](LICENSES/CC-BY-4.0.md).

Software contained in this repository is licensed under [MIT](LICENSES/MIT.md).
