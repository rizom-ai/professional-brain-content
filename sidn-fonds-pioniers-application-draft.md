# SIDN Fonds Pioniers — Application draft

*Target: SIDN Fonds Pioniers. Max €10,000, rolling, max 6 months runtime, ~6-week response. Terms verified 2026-08-04.*

**Apply as a natural person, not Rizom B.V.** The organisation route requires a KvK extract and a jaarrekening; the BV is pre-revenue with €0. Applying personally also matches the NLnet split, where Jan Hein takes the standards work and Rizom takes the implementation.

## Working title

**Leave With Everything** — a provable data-portability guarantee for self-hosted knowledge infrastructure.

## The problem

Organisations are moving their institutional memory into AI-powered SaaS. The decisions, the context, the reasoning — all of it becomes the vendor's asset, held in the vendor's schema, queryable only through the vendor's model. Every one of these products advertises an export. Almost none of them can demonstrate that the export is *complete*, or that what comes out can be loaded into anything else.

That gap matters most for the organisations least able to absorb it: libraries, broadcasters, universities, museums, care institutions. They are being asked to commit their memory to infrastructure they cannot verifiably leave.

## What gets built

An open, testable portability standard, and the tooling to prove conformance:

1. **A portability specification.** What a complete export of an organisational knowledge base must contain — content as portable markdown, metadata, relations between entities, and provenance. Written to be implementable by anyone, not only by Rizom.
2. **A reference exporter and importer** (AGPL), producing an archive plus a machine-readable *deed of ownership* describing exactly what the archive contains.
3. **A conformance test.** Round-trip verification: export a full brain, import it into a fresh independent instance, and produce a loss report. If something cannot survive the trip, the test says so rather than hiding it.
4. **Published findings.** Documentation, the spec itself, and a written account of what actually breaks in round-tripping organisational knowledge — the failure modes are the useful part and nobody publishes them.

## Why it fits SIDN

- **Sterk internet.** Lock-in in knowledge infrastructure is a structural dependency problem, not a product complaint. A verifiable exit is what makes ownership real rather than advertised.
- **Public interest.** The spec and tooling are usable by any project, not just Rizom Brains. The beneficiaries are the public institutions most exposed to lock-in.
- **Survives the funding period.** AGPL, in a public repository, with the spec published independently of any implementation.
- **Results are shared.** The specification, the conformance test and the failure-mode write-up are the deliverables, not by-products.
- **Six months, bounded.** One self-contained piece with a demonstrable end state.

## Budget — €10,000

| Item | |
|---|---|
| Specification and data model design | €2,500 |
| Reference exporter / importer implementation | €4,000 |
| Conformance test suite and loss reporting | €2,000 |
| Documentation, spec publication, findings write-up | €1,500 |
| **Total** | **€10,000** |

## Relationship to the NLnet application

This is **M2 (portability guarantee)** from `nlnet-ngi-zero-application-draft`. If SIDN funds it, carve M2 out of the NLnet ask — €50k across five milestones becomes €40k across four — and disclose the relationship in both applications. The NLnet note already flags that same-work-twice reads as cap-gaming; this is the same principle applied across funders rather than within one.

## Correction to carry

This grant **cannot** co-finance the Stimuleringsfonds application. Cofinanciering there is defined as additional funding *for that project*; a SIDN grant for infrastructure work does not qualify as co-financing for a separate Lane A project. The Stimuleringsfonds ~€6.25k needs its own source — own income is the realistic one.

## Still needed before submitting

- **Short video pitch** — required by FundPro. `cht-video-script` may be partly reusable.
- FundPro questionnaire.
- No KvK extract or jaarrekening required when applying as a natural person.