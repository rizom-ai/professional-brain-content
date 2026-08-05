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

## Video pitch — script

*FundPro requires a "korte videopitch". Exact length not published; written to ~2:00 at a natural Dutch pace (~250 words, ~130 wpm). Register follows `cht-video-script`: calm, declarative, no founder-pitch cadence.*

**[0:00 — Hook | ~15s]**

Ik ben Jan Hein Hoogstad. Elke organisatie die haar kennis in een AI-platform zet, krijgt een exportknop. Bijna geen enkele kan aantonen dat wat eruit komt volledig is.

**[0:15 — Waarom het ertoe doet | ~25s]**

Dat klinkt technisch. Dat is het niet. Bibliotheken, omroepen, universiteiten, zorginstellingen — juist de organisaties die het zich niet kunnen veroorloven — leggen hun geheugen nu vast in infrastructuur die ze niet aantoonbaar kunnen verlaten. Eigenaarschap dat je niet kunt controleren is geen eigenaarschap. Het is een belofte.

**[0:40 — Wie ik ben | ~20s]**

Ik bouw twintig jaar software, en sinds 2019 kennisinfrastructuur met AI. Ik bouwde Public Badges, een keurmerkframework dat in de Nederlandse media-, cultuur-, onderwijs- en zorgsector is ingezet. Nu bouw ik Rizom Brains: open source, self-hosted, AGPL.

**[1:00 — Wat ik ga maken | ~30s]**

Wat ik met dit project wil maken is geen product maar een norm. Een specificatie van wat een volledige export moet bevatten. Een referentie-implementatie die exporteert én importeert. En een conformiteitstest: exporteer een heel brein, importeer het in een verse, onafhankelijke installatie, en rapporteer wat er onderweg verloren gaat. Als iets de reis niet overleeft, zegt de test dat — in plaats van het te verbergen.

**[1:30 — Wat er achterblijft | ~20s]**

De specificatie is bruikbaar voor iedereen, niet alleen voor mijn eigen platform. Alles staat onder AGPL in een openbare repository. En ik publiceer wat er stukgaat — die faalgevallen zijn het nuttigste deel, en niemand schrijft ze op.

**[1:50 — Slot | ~10s]**

Een sterk internet betekent dat je kunt vertrekken. Dit project maakt dat controleerbaar.

**[2:00 — einde]**

### Marked cuts (if running over)

1. Cut *"Dat klinkt technisch. Dat is het niet."* (saves ~6 words / 3s) — the institution list still carries it.
2. Compress the credential line to *"Ik bouw twintig jaar software, en sinds 2019 kennisinfrastructuur met AI."* (saves ~20 words / 9s) — drops Public Badges, which is in the written application anyway.
3. Cut *"in plaats van het te verbergen"* (saves 5 words / 2s).

### Delivery notes

- Talking head, one take. No slides — the point is a person worth funding for six months.
- Same register as the CHT video: declarative, unhurried, zero hype. One beat of silence after the hook.
- The strongest line is the last one. Land it and stop; don't add a thank-you.
- Record horizontal, quiet room, natural light, look at the lens. Three takes, pick the warmest rather than the most polished.
- **English version available if preferred** — SIDN is a Dutch fund and the applicant is a native speaker, so Dutch is the default, but the project itself is international and open-source.

## Relationship to the NLnet application

This is **M2 (portability guarantee)** from `nlnet-ngi-zero-application-draft`. If SIDN funds it, carve M2 out of the NLnet ask — €50k across five milestones becomes €40k across four — and disclose the relationship in both applications. The NLnet note already flags that same-work-twice reads as cap-gaming; this is the same principle applied across funders rather than within one.

## Correction to carry

This grant **cannot** co-finance the Stimuleringsfonds application. Cofinanciering there is defined as additional funding *for that project*; a SIDN grant for infrastructure work does not qualify as co-financing for a separate Lane A project. The Stimuleringsfonds ~€6.25k needs its own source — own income is the realistic one.

## Still needed before submitting

- Record the video pitch (script above).
- FundPro questionnaire — the fields are behind their login, so they need filling in the system itself. Everything above should map onto them.
- No KvK extract or jaarrekening required when applying as a natural person.
- Decide whether to carve M2 out of the NLnet ask now or after a SIDN decision (~6 weeks).