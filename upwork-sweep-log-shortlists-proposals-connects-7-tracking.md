---
title: 'Upwork Sweep Log — shortlists, proposals, Connects (§7 tracking)'
visibility: restricted
---
# Upwork channel — status and decisions

Tracking note for P2/P3 of `upwork-plan-fast-income-channel-assisted-human-approved`.

**Status and decisions only.** The full per-sweep evidence log — 33 sweeps, reject
distributions, every killed candidate with its reason, every send attempt — lives on disk at
`~/Documents/upwork-assets/sweep-log.md` and is canonical.

Last updated: 2026-09-10, evening.

---

## §7 running totals

| Metric | Total to date |
|---|---|
| Proposals sent (§7 denominator) | 6 |
| Strategic sends (outside §7 math) | 1 |
| **Viewed** | **0 of 7** |
| Replied to a proposal | 0 |
| **Inbound via profile** | **1** — Lorenzo Polhout / MKBFlow, 8 Sep; a priced offer is on the table |
| Interviews | 0 |
| Contracts | 0 |
| Connects spent | 147 (97 proposals + 35 IDV badge + 15 proposal 7); balance 45 |
| Catalog offerings live | 8 |
| Catalog orders | **0** |

§7's reply-rate criteria never fired — 6 proposals is below the 20 at which reply rate becomes
readable. Its other clock is the operative one: *first contract by week 3 = on track, nothing
by week 4 → Upwork is not the channel.* Channel opened 26 August; week 4 ends 23 September.

---

## Live threads

### Lorenzo Polhout — MKBFlow (Utrecht)

Arrived 8 September by finding the profile directly — not via any proposal, invite or
Catalog listing. Client record: 73 % hire rate, $17K+ spent across 8 hires, $75.76/hr average
paid, payment verified, on the platform since July 2023. The only client encountered in
33 sweeps that clears every economic check.

MKBFlow is **pre-launch**: no clients, no platform yet. The plan is an acquisition agency →
a human operator (analysis, business case, closing, onboarding, escalations) → a Developer
(builds workflows, integrations and the platform, stays technically responsible) → an AI
operational layer. Three AI roles: a Relationship Manager for post-live client contact, a
General Manager watching deadlines, SLAs, incidents, payments and KPIs, and a technical
assistant for the Developer.

**Offer delivered 10 September, 19:04:** a written architecture document — platform
requirements the AI layer imposes (logged events, explicit state transitions, structured
client data, audit trail), role sequencing, control and escalation design including a
per-category measurement gate for Relationship Manager autonomy, a build estimate as a range
with stated assumptions, monthly running costs at several client volumes, and the shape of
ongoing involvement. **€2.000 fixed price**, two weeks from the later of a funded contract and
receipt of three items (what the ten workflows do; what the platform will be built on; which
channel clients communicate through), credited against the build. Closes with "Zullen we het
zo doen?".

**If he accepts:** an Upwork fixed-price contract with one milestone funded into escrow before
any work. The six sections and the boundary — not a build quote, no code, no prototype — go in
the milestone description. Amount in USD on the day. A withdrawal method must exist before
funds can leave Upwork; it is still not set up.

Sequence: his opener 8 Sep 00:26 → short Dutch reply → his brief (AI-first agency) → a reply
asking for two or three processes described properly → his re-scope to the three AI roles with
eight questions including price → a reply answering feasibility, controls and what is reliably
automatable today, declining to price without material, and offering the €2.000 scoping →
his disclosure that MKBFlow is pre-launch, asking whether that changes the proposal → the
offer above.

### Proposal 7 — Senior AI Engineer, $6,000 fixed

Sent 9 September, 15 Connects, bid at the full ask. Agent orchestration, retrieval, MCP in the
mandatory skills. Client: Karachi account created 14 August, 2 jobs posted, 0 % hire rate, no
spend history, payment verified. The first bid ever placed into the segment the suspended
never-hires rule used to delete unseen. Insights at last check: 24 proposals, 23 unopened,
ours unopened, 0 shortlisted, 6 messaged; the messaged average had fallen from $6,000 to
$5,004.

---

## Diagnosis — corrected 2026-09-06

Every submitted proposal carries an Insights panel at `/nx/proposals/<id>`. Read for the
first time on 6 September, across the six proposals then live: **347 of 383 competing
proposals unopened (91 %)**, all six of ours unopened, and shortlisting visibly happening
without opening (one job: 0 opened, 17 shortlisted). Clients shortlist off the list row —
photo, headline, badge, total earned, rate, first two lines. The proposal body is not skimmed;
it is never loaded. Proposal quality is therefore not the lever; the row is.

The earlier diagnosis — "proposals reach clients and lose on trust signal" — was wrong. They
are not read.

Peer set, measured: the average applicant on those jobs carried $18K–$187K lifetime earned,
11–50 jobs, 4–6 years on the platform, 97–100 % JSS.

**Rate holds at $150.** On every job where a client messaged anyone, the messaged bids
averaged at or above the field.

---

## The reachable pool

The "never-hires trap" rule killed every client with $0 spend or a low hire rate for
30 sweeps and was never tested. On the 6 September pool it was deleting 106 of 323 on-thesis
listings unexamined. **Suspended**, replaced by spend-per-hire (lifetime spend ÷ hires; under
~$50 a contract is a review farm regardless of the spec).

What the pool contains: clients who hire constantly at $5–100 and leave five-star reviews —
e.g. a $100 job from an account with 178 hires and $3.1K spent ($17 per contract,
$6.01/hr average paid). The clients who will hire a profile with no reviews are largely the
ones for whom no reviews is the point. Decision, 6 September, in the human's words: "they are
vultures." No bid placed there.

---

## Account state

| Item | State |
|---|---|
| **Rising Talent** | **Awarded 9 September** via Upwork's invitation route (earnings were $0). Badge on profile, proposals and Catalog projects. +30 Connects. |
| **Identity verification** | Verified 6 September, valid to September 2029 (35 Connects) |
| Consultations | Unlocked by the badge, no Connects needed to list. **Not set up.** |
| Withdrawal method | **Not set up** — up to 3 days to activate. Blocks any payout. |
| Profile completeness | 100 % |
| Freelancer Plus | Active — 0 % fee on Direct Contracts |
| Work history | No items |

Direct Contracts (bring a non-Upwork client, 0 % fee on Plus, feedback counts toward JSS and
badges) were proposed on 6 September and **rejected by the human**.

---

## Angles tested and closed

| Angle | Verdict |
|---|---|
| Rare-tech arbitrage (Elixir, Clojure) | Dead — 2 Elixir jobs, 1 Clojure, both bid-swarmed |
| Language arbitrage (German, Dutch) | Real moat, wrong goods — guards voice, UGC, support, transcription, not architecture. Note: the one inbound client is Dutch and found the profile directly |
| Infra / DevOps widening (BUCKET-B) | Retired 4 September — five runs, nothing bid-worthy, ~150 tiles of noise per sweep |
| Availability badge | 14 Connects/week. Cancelled unused |
| Direct Contracts | Rejected by the human |
| Boost | Not attempted |
| Review-farm bids ($5–100) | Rejected by the human |

---

## Loop status

**Cron v8, once daily at 07:53**, session-only, re-armed 10 September after an Upwork outage,
expires ~17 September. Checks the two live threads before any sweeping; opens Insights on live
proposals; treats tile bid counts as a floor; applies page-only checks and spend-per-hire at
verification; reports findings without recommendations.

## Sending — what proves delivery

Established 9–10 September across several silent failures:

- Pre-contract, Upwork blocks any message naming a third-party messaging platform (WhatsApp,
  Telegram, Signal, Slack, Skype, Discord). Generic words pass.
- A message is delivered only when its story container lacks the `blocked` class and the
  sidebar preview shows it. Text presence, absence of banner text, and a 200 on the POST are
  all false positives — failed and blocked bubbles carry the full text, banners vary and vanish
  on reload, and blocked messages also return 200.
- Proposal form: the milestone description field needs real keystrokes; the due date wants
  DD-MM-YYYY; fixed-price sends pop an escrow modal; success is the URL flipping to `?success`
  and the job appearing under Submitted proposals.
