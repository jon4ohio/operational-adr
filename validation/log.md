# Validation Log

**Status:** Phase 4 — adoption validation  
**Date:** 2026-07-10

Documents adoption attempts against [spec/adr-v1.0.md](../spec/adr-v1.0.md). v1.0 success criterion: an adopter without access to portfolio or Anchor repositories can adopt the practice.

---

## Publish note

**v1.0 shipped** (2026-07-10). Repository published with unified project statement in [README.md](../README.md).

**Specification independence:** Adopters need only this repository and [spec/adr-v1.0.md](../spec/adr-v1.0.md)—not portfolio or Anchor access. Origin repositories explain provenance; they are not adoption prerequisites.

Report adoption or friction via issues; entries will be logged here.

---

## Attempt 1 — Self-adoption (reference implementation)

**Adopter:** Project maintainer (dogfooding)  
**Corpus access:** Full (author) — simulates blind adoption by following only README → spec → decisions  
**Date:** 2026-07-10

### Steps followed

1. Read [README.md](../README.md) for problem statement and architecture
2. Read [spec/adr-v1.0.md](../spec/adr-v1.0.md) for file layout and tier structure
3. Created `decisions/` with three Tier 1 ADRs covering packaging methodology, spec shape, and meta-governance
4. Created `decisions/index.md` and `decisions/LOG.md`
5. Verified conformance against spec §11 checklist

### Conformance checklist

| Requirement | Result |
|-------------|--------|
| ADRs in documented directory with `ADR-NNN-short-title.md` naming | Pass |
| Tier 0 sections in every ADR | Pass |
| Tier 1 sections in dogfood ADRs | Pass |
| Recording threshold documented | Pass (ADR-003) |
| Index present | Pass (3 ADRs; early but demonstrates pattern) |
| Immutability / supersession path documented | Pass (in ADRs + spec) |

### Friction observed

| Friction | Severity | Resolution |
|----------|----------|------------|
| Tier 0 vs Tier 1 choice unclear for first ADR | Low | Spec §9 tier guide sufficient after reading model §10 |
| "Evidence-first" naming confusion | Med | README clarification + ADR-001; recommend adopters copy README paragraph |
| Relationship verbs optional at Tier 0 | Low | Documented in spec §2; portfolio verbs used in dogfood ADRs |
| No tooling (lint, template generator) | Low | Out of scope v1.0; markdown-only adoption works |

### Outcome

**Pass.** An adopter reading only this repository (without portfolio/Anchor) can:

- Understand when to write ADRs
- Create Tier 0 or Tier 1 ADRs from spec templates
- Maintain index and LOG
- Trace model elements to capture provenance via `model/traceability.md`

### Open items for v1.1

- Template generator or `adr new` CLI (optional tooling)
- Worked example: supersession chain in reference impl (none yet)
- External adopter without author access (pending real-world attempt)

---

## Attempt 2 — Anchor (one adopter among many)

**Adopter:** Anchor meta-repo (https://github.com/jon4ohio/anchor)  
**Corpus access:** Maintainer; Anchor was secondary extraction corpus during capture—shared history, **not required for other adopters**  
**Date:** 2026-07-10

### Integration approach

- Anchor ADR contract unchanged (minimal)
- Evidence-First ADR listed as compatible format (not absorbed)
- [ADR-004](https://github.com/jon4ohio/anchor/blob/main/docs/decisions/ADR-004-evidence-first-adr-compatible-format.md): future framework ADRs **MAY** use EFA v1.0 as **preferred** rich format—not mandatory
- ADR-004 written in Evidence-First ADR Tier 1 (first Anchor use of format)
- Spec linked at `v1.0.0` tag; not copied into Anchor

### Policy note

Adoption is permissive (MAY/preferred) by design. Strengthening to SHOULD/mandatory deferred until sustained natural use produces evidence (~6 months or three new framework ADRs).

### Friction observed

| Friction | Severity | Resolution |
|----------|----------|------------|
| (none yet) | — | Observe during next framework ADRs |

### Outcome

**In progress.** Anchor is one adopter—listed alongside future Project A/B/C style adopters, not as a required step in a universal lifecycle. Format friction routes to this repo's issues; framework friction stays in Anchor evidence.md.

---

## Attempt 3 — External adopter (non-Anchor)

**Status:** Not yet attempted  
**Trigger:** First external user outside Anchor/portfolio reports adoption or friction

---

## Peer comparison (optional)

See [analysis/comparison-v1.0.md](../analysis/comparison-v1.0.md) — descriptive comparison with Nygard and MADR after model exists. Does not reshape capture or spec.

---

## v1.0 validation verdict

| Criterion | Met? |
|-----------|------|
| Model with full traceability | Yes |
| Spec derived from model | Yes |
| Reference implementation | Yes (3 ADRs, index, LOG) |
| Adoption without source repos | Yes (self-adoption blind to corpus) |
| External adopter (non-Anchor) | Pending |
| Specification independent of origin | Yes (v1.0 publish milestone) |
| Anchor adopter (one among many) | In progress (MAY/preferred policy) |

**v1.0 packaging complete.** External validation remains open for promotion claims.
