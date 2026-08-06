# Offcourse on Brains — scope, what exists, funding fit

Worked up 2026-08-05, from Jan Hein's proposal to rebuild Offcourse on the brains substrate. Framing constraint set at the same time: **capitalise on existing work; only build new things if there is no angle to monetise what already exists.** This note is written against that test.

## What it is

Offcourse's original thesis was crowdlearning: practitioners curate, structure and share knowledge across distributed networks. Not courses delivered downward — knowledge assembled by the people who hold it. Between 2013 and 2024 the idea was right and the substrate had to be built from nothing.

On brains it becomes concrete. Every participant has their own brain: personal, portable, self-hosted, theirs. A cohort has a shared brain. Knowledge moves between them by consent. A "course" is not a content package — it is a constellation of brains around a shared question, with the shared brain as the group's memory.

**That is already what is being sold.** `pilot-proposal-a-cohort-brain-for-the-ai-datacampus` describes a founding team in two rings — a core working in the brain daily, a ring contributing and retrieving — with "personal knowledge that stays portable, under its owner's control". That is crowdlearning with a different name in front of it.

## Why the name is worth reviving

Not nostalgia. Three practical things:

- **Provenance.** Eleven years of continuous open-source development is a credential that a new project cannot buy, and it is exactly what grant assessors and institutional buyers weigh.
- **Comprehension.** "A cohort brain" needs explaining. "Offcourse, rebuilt on infrastructure you own" does not — not to PublicSpaces members, not to a campus coordinator, not to NLnet.
- **The domain and the record exist.** offcourse.io, the repos, the history.

The honest counterweight: Offcourse was wound down in December 2024. Reviving a dead project needs a reason, and "the substrate changed" is the only good one. It happens to be true — markdown+git, MCP, agents and per-user provisioning did not exist in 2013 and are what the original idea needed.

## What already exists

This is the point of the proposal. Nearly all of it is built:

- **The runtime.** brains monorepo, 5,700+ commits, AGPL. MCP server with OAuth, plugin system, site generation, deployment tooling.
- **Multi-tenant provisioning.** `pilot.yaml`, per-user `.env`, shared `brain-${brainVersion}` image, Kamal deploy and reconcile workflows — see `operator-playbook`. The machinery for running brains for many people is done.
- **A live fleet, and it is discoverable.** rizom.ai's map shows **6 agents indexed** — becca, rizom brain docs, jo, mindinn, sam, yeehaa — registered and visible on the public network map (checked 2026-08-05).
- **Onboarding.** `rover-pilot-user-onboarding` is a complete first-time-user document: connection, first five minutes, Obsidian/git workflow, private per-user content repos, wishlist capture.
- **Bidirectional sync.** directory-sync carries markdown between a private git repo and the brain, so participants can work in Obsidian and the brain picks it up.
- **A priced commercial offer.** The Datacampus proposal: scoping sprint → Phase 1 build → Phase 2 licence.
- **The method.** TMS, the Protocol Canvas, and the workshop that seeds a group's knowledge — see `tms-services-plan`.
- **The name and eleven years behind it.**

## What is genuinely missing

Short list, and narrower than it first appeared:

1. **Constellations.** Agent discovery and the registry work — six agents are indexed. What reads **0** is constellations: no group has formed by substance yet. That may be a build gap in the grouping logic, or simply too few agents with too little shared public substance to cluster on. Worth establishing which before scoping any work against it.
2. **Consent-based sharing.** "Each partner decides what it shares" is in the Datacampus proposal as a promise. Per-entity visibility exists; cross-brain selective sharing does not.
3. **Group curation workflows.** How a cohort actually works together — contributing, curating, reviewing, surfacing what the group knows that no individual does. This is the crowdlearning part, and it is the genuinely unbuilt piece.

Everything else is assembly and naming.

## Monetisation — the primary test

No new commercial model is required. What exists:

- **The scoping sprint** is the nearest cash: a fixed fee at the level of one build month (€3–5k), credited against the pilot if it proceeds. Smallest sellable unit, already designed, and it sits alongside the €5,000 Knowledge Session as a warm-contact ask.
- **Phase 1** — Rizom retainer €3–5k/month, plus €10–20k of build resourced by the partners in staff time or budget.
- **Phase 2** — licensing as it extends across an institution.
- **Per-seat personal brains** for cohort members, on provisioning that already runs.

Note the pricing conflict flagged in `rizom-product-plan`: the Datacampus figures predate the locked bands in `fundraising-strategy-and-decisions`. Reconcile before quoting.

## Funder fit

**NLnet — the right one.** Opens 3 Sept, closes 3 Nov, €50k, Lane B. The existing draft's M3 (AT Protocol federation, selective sharing between self-hosted brains) and M4 (open lexicon + SDK) *are* the missing layer above. The draft already funds Offcourse-on-brains without saying so. Reframing it around crowdlearning infrastructure rather than abstract portability gives it a public-interest narrative and a concrete user, which is what NGI funds. Note the demo is stronger than the draft implies — six agents are already indexed on a live public map.

**SIDN Pioniers — a bounded carve-out only.** €10k, six months. The consent model for sharing between brains would fit; the full scope would not. See `sidn-fonds-pioniers-application-draft`, which currently proposes a portability standard — worth reconsidering against this framing before sending the webformulier.

**Stimuleringsfonds — leave it in Lane A.** The digital-culture field definition is artistic; this is infrastructure. Keep that round for the research and writing.

## Open questions

- Does Offcourse come back as the product name, or as heritage inside Rizom Brains? Two brands is a cost a one-person operation may not want.
- Datacampus is the first customer for this whether or not it is called Offcourse. Does renaming help or complicate a live proposal?
- Are zero constellations a missing feature or a cold-start problem? Different answers point at different work.
- The delivery constraint in `rizom-product-plan` still applies: one person can currently run a pilot, and cohort work is more delivery-heavy than a single team brain.