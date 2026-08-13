# SIDN Fonds Pioniers — Application draft

*Max €10,000. Rolling — the 2026 call runs to 31 December 2026, 13:00 Europe/Amsterdam. Max 6 months runtime. ~6-week response on the full application. Terms verified 2026-08-04 from the call page and criteria.*

**STATUS: step 2 REJECTED 2026-08-13.** Jet Veldhuis, projectcoördinator, by email. Rejected on fit with *Sterk internet*, not on quality or budget:

> *"Hoewel de aanvraag raakt aan open protocollen en decentralisatie, zien wij de voorgestelde activiteiten voornamelijk als een verkenning van kennisdeling en communityvorming. Daarbij ontbreekt voor ons een voldoende directe relatie met het ontwikkelen van internetbouwstenen of andere oplossingen die bijdragen aan het versterken van het internet."*

**➜ NEXT ACTION — file the rescoped toets on Tuesday 25 August 2026.** Text ready at `~/Documents/sidn-webform-v2.md`. Pioniers is doorlopend, so there is no deadline pressure; the date is chosen for distance from the rejection, not for a cutoff. Nothing is blocking it.

## The rejection is correct, and that decides the rewrite

Re-reading the submitted text (`~/Documents/sidn-webform.md`) against the rejection: the lexicon and the AT Protocol reference implementation were points 1 and 2 of a four-part approach, arriving after ~1200 words on institutions shedding their intellectual life, with an *Expected impact* entirely about community persistence and a closing field asking SIDN to help find a community. Read at speed, that is a community-formation project with a technical footnote. Jet read it accurately.

The irritating part — that the words "open lexicon" and "reference implementation" were present and still drew "onvoldoende directe relatie met internetbouwstenen" — does not change the conclusion. Burying the deliverable is the applicant's problem, not the reader's.

**No reply was sent.** A drafted reply asking whether the rescope would fit is at `~/Documents/sidn-fonds-reply-draft.md`, unsent and probably to stay that way: the toets *is* the cheap pre-check, so resubmitting it asks the same question at the same cost and returns a binding answer instead of an informal one.

## What changed in v2

| | v1 (rejected) | v2 |
|---|---|---|
| First sentence | The organized-networks question | What gets built: the lexicon |
| Cultural context | ~1200 words, carries the pitch | One paragraph, as origin |
| Impact claim | Communities can persist | Decentralised discovery as infrastructure |
| Community demonstration | Core of the approach (point 3) | Removed |
| Field 3 | "Will you help me find a community?" | Technical scoping question on interoperability |
| Language | English | Dutch |

## The project (v2)

**Een open lexicon voor verwijzing tussen zelfgehoste kennisbronnen.**

An open lexicon on the AT Protocol specifying how a self-hosted knowledge source publishes what it holds, in a form other independently held sources can find, connect to and cite — plus an AGPL reference implementation and a specification published independently of it.

The gap argued in ATProto terms: the protocol already provides portable identity (DIDs), a per-actor repository model, and lexicons as enforceable schema. What is missing is a lexicon for knowledge holdings. Existing lexicons describe social objects — posts, follows, likes. This one describes what a source knows and on what terms it shares.

**Deliverables (six months):**

1. The lexicon — record types for what a source publishes about its own contents: subjects, citable units, per-record visibility (public / peers only / never leaves the source). Specification published separately, implementable without my code.
2. Reference implementation under AGPL, in a public repository.
3. Working demonstration between at least two independently hosted sources finding and citing each other with no central party.
4. Published method and findings, including where it fails.

## Budget — €10,000 (revised)

| Item | |
|---|---|
| Lexicon design and published specification | €3,000 |
| Reference implementation (AGPL, public repo) | €4,000 |
| Demonstration between two independently hosted sources | €1,500 |
| Documentation, lexicon publication, findings | €1,500 |
| **Total** | **€10,000** |

The €2,000 community-demonstration line from v1 is gone; €500 moved to specification quality and €1,500 to the two-source demonstration. Structural organisational costs, overheads and salary not attributable to the project remain excluded by the criteria.

## What is asked of them in v2

Not a community. A scoping judgement: two independently hosted sources both running my reference implementation proves the lexicon works but not that it is *interoperable*, since both ends run my code. The real test is a second independent implementation built from the specification alone — which depends on someone else's time and cannot be guaranteed in six months. The question is whether SIDN counts that as core to being an internetbouwsteen, in which case the six months are built around specification quality, conformance tests and supporting a first external implementor rather than around features.

## How it sits with the other funding threads

- **NLnet / NGI Zero Open Internet Stack** (€50k, window 3 Sep – 3 Nov 2026) — M3 federation and M4 lexicon + SDK now build *on top of* this: production federation between independent instances, selective consent, SDK, portability, self-hosting. **Sequential, not overlapping** — SIDN funds specification and first implementation, NLnet hardens it. Must be disclosed in both. A completed SIDN deliverable strengthens the NLnet bid rather than competing with it.
- **ISOC Beyond the Net** (`isoc-beyond-the-net-concept-note-digital-autonomy-in-practice`) — gives civil-society organisations a memory they own.
- **Stimuleringsfonds / INC** (`stimuleringsfonds-application-organized-memory-rizom-inc`) — the community practice and cultural reflection. This is precisely the layer v1 wrongly imported into the SIDN pitch.

**Still no partners named.** Neither INC nor the ISOC NL cohort is committed. Add when real.

## Framings tried and dropped

Recorded so they don't come back round.

- **Community demonstration as the centre** (v1, rejected 2026-08-13). The reason for the rejection. Dropped: it belongs to the Stimuleringsfonds/INC thread, and importing it here made the whole pitch read as verkenning.
- **Portability standard** (first draft). Spec plus conformance test for verifiable export. Dropped: the exit-path work is already inside the ISOC project.
- **Consent layer.** How a person shares selected knowledge into a group space on revocable terms. Dropped in favour of constellations.
- **Privacy-first framing.** Wrong premise: the thesis across this work is that far too much knowledge is kept private and dies there. Openness by default, closure by exception.
- **Findability framing.** The mechanism without the question.
- **A density study.** Pioniers is idea-phase; the deliverable is *"een demo, pilot of experimenteel ontwerp"*.
- **Node counts.** "Six independently held knowledge bases" claims an independence that isn't there — the agents on the rizom.ai map are largely Jan Hein's own instances. No count is used anywhere. v2 states "at least two independently hosted sources" strictly as a deliverable, never as an existing state. The same overstatement is still in `offcourse-on-brains-scope-what-exists-funding-fit` and should come out.
- **Defensive question framing.** Permission questions — is a conceptual result acceptable, does the platform link disqualify me. Wrong posture for something anchored in a foundation and an AGPL commons.
- **A credentials sign-off.** Contradicts a pitch arguing credentials are the wrong signal. v2 closes on the public AGPL repo plus yeehaa.io running, with no meeting requested — asking for half an hour contradicts telling them a short answer is enough.

## The procedure — four steps, and FundPro is step 3

1. **Quickscan** and check the Pioniers criteria.
2. **Toets je project via het webformulier** — v1 sent 2026-08-09, rejected 2026-08-13. **v2 due 2026-08-25.**
3. **Apply via FundPro** — questionnaire, short video pitch, project plan of max 4 A4, plus KvK extract and jaarrekening only if applying as an organisation. Personal lane: apply as natural person, so neither is needed.
4. Answer within six weeks.

## Next

- **2026-08-25 — file the v2 toets** from `~/Documents/sidn-webform-v2.md`. Field lengths verified against the 3000 / 1500 / 1500 limits (2635 / 1351 / 1328).
- Do **not** send the drafted reply to Jet; the toets replaces it.
- Record a video pitch **for step 3 only**, after a positive read. Both earlier scripts are obsolete — the 2026-08-04 one pitched portability, the v1 framing pitched community.
- Project plan, max 4 A4, only at step 3.
- Re-derive the NLnet disclosure text against the sequential split before the 3 September window opens.