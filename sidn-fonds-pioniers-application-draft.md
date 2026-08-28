# SIDN Fonds Pioniers — Application draft

*Max €10,000. Rolling — the 2026 call runs to 31 December 2026, 13:00 Europe/Amsterdam. Max 6 months runtime. ~6-week response on the full application. Terms verified 2026-08-04 from the call page and criteria.*

**STATUS: v2 toets submitted 2026-08-23; Jet Veldhuis responded 2026-08-27 with five follow-up questions; answers sent 2026-08-28.** All five questions were demand-side (users, newly enabled capability, size of need, positioning against existing protocols/platforms, value for the internet as a whole) — the rescope landed; no fit objection this time, and the questions track the assessment criteria. The reply answers them in her exact order: `sidn-fonds-antwoorden-op-vragen-jet-veldhuis` (also at `~/Documents/sidn-antwoorden-jet-veldhuis.md`).

**➜ NEXT ACTION — wait for SIDN's read.** On a positive signal, move to step 3 (FundPro): record the video pitch, write the project plan (max 4 A4).

History: **v1 (step 2) REJECTED 2026-08-13.** Jet Veldhuis, projectcoördinator, by email. Rejected on fit with *Sterk internet*, not on quality or budget:

> *"Hoewel de aanvraag raakt aan open protocollen en decentralisatie, zien wij de voorgestelde activiteiten voornamelijk als een verkenning van kennisdeling en communityvorming. Daarbij ontbreekt voor ons een voldoende directe relatie met het ontwikkelen van internetbouwstenen of andere oplossingen die bijdragen aan het versterken van het internet."*

## The rejection was correct, and that decided the rewrite

Re-reading the submitted text (`~/Documents/sidn-webform.md`) against the rejection: the lexicon and the AT Protocol reference implementation were points 1 and 2 of a four-part approach, arriving after ~1200 words on institutions shedding their intellectual life, with an *Expected impact* entirely about community persistence and a closing field asking SIDN to help find a community. Read at speed, that is a community-formation project with a technical footnote. Jet read it accurately.

The irritating part — that the words "open lexicon" and "reference implementation" were present and still drew "onvoldoende directe relatie met internetbouwstenen" — does not change the conclusion. Burying the deliverable is the applicant's problem, not the reader's.

**No reply was sent to the v1 rejection.** A drafted reply asking whether the rescope would fit is at `~/Documents/sidn-fonds-reply-draft.md`, unsent and now moot: the v2 toets was the pre-check, and it drew engaged follow-up questions instead of a second rejection.

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

*(Jet's 2026-08-27 email did not answer this field-3 question; deliberately not re-raised in the antwoorden reply — her questions show the assessment is moving, and the question stays on file in the toets.)*

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
- **A credentials sign-off.** Contradicts a pitch arguing credentials are the wrong signal. v2 closes on the public AGPL repo plus yeehaa.io running, with no meeting requested — asking for half an hour contradicts telling them a short answer is enough. Extends to the antwoorden reply: no title claims ("door mijn werk voor PublicSpaces", not "tech lead"), Rizom named as an exploration route, not as a company, and rizom.ai deliberately not linked (product frame; the central agent map would muddy the exists/doesn't-exist line).

## The procedure — four steps, and FundPro is step 3

1. **Quickscan** and check the Pioniers criteria.
2. **Toets je project via het webformulier** — v1 sent 2026-08-09, rejected 2026-08-13. v2 sent 2026-08-23; follow-up questions received 2026-08-27, answers sent 2026-08-28.
3. **Apply via FundPro** — questionnaire, short video pitch, project plan of max 4 A4, plus KvK extract and jaarrekening only if applying as an organisation. Personal lane: apply as natural person, so neither is needed.
4. Answer within six weeks.

## Next

- ✅ **Answers to Jet's five questions sent 2026-08-28** — text in `sidn-fonds-antwoorden-op-vragen-jet-veldhuis` (local: `~/Documents/sidn-antwoorden-jet-veldhuis.md`). Now waiting on SIDN.
- Record a video pitch **for step 3 only**, after a positive read. Both earlier scripts are obsolete — the 2026-08-04 one pitched portability, the v1 framing pitched community.
- Project plan, max 4 A4, only at step 3.
- Re-derive the NLnet disclosure text against the sequential split before the 3 September window opens.