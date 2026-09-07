---
title: 'Upwork Sweep Log — shortlists, proposals, Connects (§7 tracking)'
visibility: restricted
---
# Upwork channel — status and decisions

Tracking note for P2/P3 of `upwork-plan-fast-income-channel-assisted-human-approved`.

**Status and decisions only.** The full per-sweep evidence log — 30 sweeps, reject
distributions, every killed candidate with its reason — lives on disk at
`~/Documents/upwork-assets/sweep-log.md` and is canonical.

Last updated: 2026-09-06, after Sweep 30 and the first read of the Insights data.

---

## §7 running totals

| Metric | Total to date |
|---|---|
| Proposals sent (§7 denominator) | 5 |
| Strategic sends (outside §7 math) | 1 |
| **Viewed** | **0 of 6** |
| Replied | 0 |
| Interviews | 0 |
| Contracts | 0 |
| Connects spent | 132 (97 proposals + 35 IDV badge); balance 30 |
| Catalog offerings live | 8 |
| Catalog orders | **0** (~150 views/30 days) |

§7's reply-rate criteria never fired — 5 proposals is below the 20 at which reply rate becomes
readable. Its other clock is the operative one: *first contract by week 3 = on track, nothing
by week 4 → Upwork is not the channel.* Channel opened 26 August; week 4 ends 23 September.

---

## Diagnosis — corrected 2026-09-06

The 2026-09-01 diagnosis recorded here previously said *"proposals reach clients and lose on
trust signal."* **That was wrong**, and it was wrong because the assistant never opened the
Insights panel that sits one click from `/nx/proposals/` — a page checked twice daily for
eleven days.

Every submitted proposal carries an Insights panel at `/nx/proposals/<id>` with hiring
activity, the full competing-bid distribution and the average competitor's profile. Read for
the first time on 2026-09-06:

| Job | Bids | Unopened | Opened | Shortlisted | Messaged |
|---|---|---|---|---|---|
| Claude Cowork Expert | 25 | 25 | 0 | 0 | 0 |
| Knowledge architect, agri | 42 | 37 | 5 | 0 | 3 |
| Maropost Neto search | 52 | 42 | 10 | 0 | 3 |
| AI Transformation Consultant | 40 | 24 | 16 | 0 | 0 |
| Automation Specialist | 170 | 165 | 5 | 7 | 3 |
| Agent Setup Expert | 54 | 54 | 0 | 17 | 5 |
| **Total** | **383** | **347** | **36** | **24** | **14** |

**All six read "Your proposal hasn't been opened yet."** They do not reach clients and lose.
They are not read.

**91 % of all proposals on these jobs went unopened** — 347 of 383. Clients open roughly one in
eleven.

**Shortlisting happens without opening.** Agent Setup Expert: 0 opened, 17 shortlisted.
Clients shortlist off the list row — photo, headline, JSS badge, total earned, rate, first two
lines. §5's "the client sees only the first two lines" was right and understated: the body is
never loaded. **Proposal quality therefore cannot be the lever.** The row is the product.

**Peer set, measured:** average applicant on these six jobs carries $18K–$187K lifetime
earned, 10.9–50.1 jobs, 4–6 years on platform, 97–100 % JSS.

**Rate: hold at $150.** On both jobs where clients messaged anyone, messaged bids averaged
*above* the field ($70.65 vs a $42.13 field; $75.80 vs $56.85). Discounting moves toward the
segment that does not hire.

---

## The reachable pool, and why it is not worth entering

The assistant's "never-hires trap" rule killed every client with $0 lifetime spend or a low
hire rate, on all 30 sweeps, and **was never tested — not one bid ever went to that segment.**
It also inverted its own evidence: it was recorded as "5-for-5: perfect on-thesis spec from a
0 %-hire/$0-spend client", which says the best-matched specs *come from* new clients. That is
an argument for bidding on them, written down as a reason to skip them. Measured on the
2026-09-06 pool, it was deleting **106 of 323 on-thesis listings** — about a third of the
addressable market — unexamined, every sweep. Rule suspended; replaced by spend-per-hire.

Inverting it surfaced what that pool actually holds. Two live, on-thesis jobs from clients who
hire constantly and leave 5-star reviews:

| Job | Price | Client |
|---|---|---|
| Thought Partner and Builder for Agentic Systems | $100 fixed (bid range $100/$100/$100) | 227 posted, 178 hires, $3.1K spent = **$17/contract**, **$6.01/hr avg paid**, 149 reviews all 5.00 |
| AI Agent Consultant — OpenClaw vs Nous Hermes | $5 fixed | 10 posted, 6 hires, $15 spent, 60 % hire rate, 3 reviews all 5.00 |

The Thought Partner spec is the best-written seen on the platform — company brain with
citations, agentic workflows with approval gates, evals and regression tests on agent output,
explicitly not n8n/Make/Zapier — attached to a client whose average contract is $17.

**The finding, which is not a filter problem:** the clients who will hire a profile with no
reviews are largely the ones for whom no reviews is the point, because they pay $17 and cannot
attract anyone else. Everyone above that tier filters on JSS and never opens the proposal —
the measured 91 %. The entry price to this channel is working at $5–100 until enough five-star
ratings accumulate to become visible to clients who are not doing this.

**Decision, 2026-09-06, in the human's words: "they are vultures."** No bid placed. Connects
held at 30.

---

## Account state

| Item | State |
|---|---|
| Profile completeness | 100 % |
| **Identity verification** | **Verified 2026-09-06, valid to Sep 2029** (cost 35 Connects) |
| Withdrawal method | **Not set up** — up to 3 days to activate |
| Rising Talent | Not held. Needs withdrawal method + 4.8★ + $250 earned in 12 months (or Upwork invitation). Gates the Consultations product, which is why §3's Consultations layer was never available |
| Freelancer Plus | Active — 0 % fee on Direct Contracts |
| Work history | No items |

**Direct Contracts** (`/ab/flservices/contracts`) let a non-Upwork client be invited to a
contract at 0 % fee on Plus, and Upwork states the feedback counts toward JSS, Rising Talent,
contract count and earnings. Proposed 2026-09-06 and **rejected by the human** — a client from
his own network paying through Upwork is not Upwork producing anything.

---

## Angles tested and closed

| Angle | Verdict |
|---|---|
| Rare-tech arbitrage (Elixir, Clojure) | Dead. 2 Elixir jobs, 1 Clojure across the period, both bid-swarmed |
| Language arbitrage (German, Dutch) | Real moat, wrong goods — guards voice recording, UGC, support, transcription, not architecture |
| Badges | None held; not acquirable without history |
| Availability badge | 14 Connects/week under "Promote with ads". Not free. Cancelled unused |
| Infra / DevOps widening (BUCKET-B) | Retired 2026-09-04. Five runs, zero bid-worthy candidates; ~150 tiles of noise per sweep |
| Direct Contracts | Rejected by the human |
| Boost | Not attempted. Would buy one top slot for 30–121 Connects against a row that still shows no history |

---

## Loop status

**Cron v7, once daily at 07:53**, session-only, armed 2026-09-06, expires ~2026-09-13. Cut from
twice daily — the second pass routinely deduped to zero new tiles.

The prompt now: opens the Insights panel every run (an opened proposal would be the first real
signal this channel has produced); treats tile bid counts as a floor, never fact (they
understated actuals by 2–10× on all six jobs); applies the four page-only checks plus
spend-per-hire at verification; keeps the tool/credential/discipline-fluency and on-thesis
rules; and reports findings without recommendations.
