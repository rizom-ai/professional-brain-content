---
title: 'Upwork Sweep Log — shortlists, proposals, Connects (§7 tracking)'
visibility: restricted
---
# Upwork channel — status and decisions

Tracking note for P2/P3 of `upwork-plan-fast-income-channel-assisted-human-approved`.

**This note carries status and decisions only.** The full per-sweep evidence log —
26 sweeps, reject distributions, every killed candidate with its reason — lives on disk at
`~/Documents/upwork-assets/sweep-log.md` and is canonical. Do not mirror it here.

Last updated: 2026-09-04, after Sweep 26.

---

## §7 running totals

| Metric | Total to date |
|---|---|
| Proposals sent (§7 denominator) | 5 |
| Strategic sends (outside §7 math) | 1 |
| Viewed | — |
| Replied | **0** |
| Interviews | 0 |
| Contracts | 0 |
| Connects spent | 97 (balance 65) |
| Catalog offerings live | 8 |
| Catalog orders | **0** (158+ cumulative views) |

Strategic sends are relationship bets with no live project behind them. They spend real
Connects but sit outside the reply-rate denominator, so the kill criteria only measure
proposals that could convert on the plan's timescale.

**Against §7's gauges:** 5 proposals is below the 20 at which reply rate becomes readable.
The kill criteria have not fired. But §7's other clock has: *first contract by week 3 = on
track, nothing by week 4 → Upwork is not the channel*. The channel opened 26 August. Week 4
ends 23 September.

---

## Diagnosis (2026-09-01, unchanged since)

Six proposals, zero replies. **Four of the six jobs were actively interviewing other
candidates** while ours sat unanswered — so proposals reach clients and lose on trust signal,
not on fit or on rate.

The binding constraint is a profile reading **Work history: No items** in a market where every
visible competitor carries 29–541 reviews and a Top Rated badge. The Catalog shows the same
gate from the other side: eight approved offerings, 158+ views, zero orders, against
comparables at $199 with 4.9★ and 69 reviews.

This is not a positioning problem and not a volume problem. Bidding harder does not move it.

**Consequence:** Upwork was demoted from the fast-income channel to a low-cost watch on
2026-09-01. The primary channel is now warm network activation — see
`~/Documents/network-outreach/` and the separate working thread.

---

## The review-acquisition bet

Catalog is a *purchase*, not a bid: it bypasses Connects and bid ranking entirely. So the
product being bought is the first review, not the work.

Ladder as it now stands: **$95 → $200 → $600–750 → $1,500–1,800 → $6,000.**
The $95 "written second opinion on one AI architecture decision" is the entry bet, live since
2026-09-03. Three views, no orders as of Sweep 26.

This supersedes §3's Consultations layer, which does not exist as a separate Upwork product —
it folded into Catalog.

---

## Send rule (amended 2026-08-28, supersedes §8's blanket wording)

No unattended submission, ever. Every send requires explicit per-job approval of the reviewed
draft. The click itself may be executed by the assistant when directed ("human-directed
send"). Sweeps never auto-send; drafts always come back for review first.

---

## §4 filter as it now stands

**At harvest time** (search-tile signals only): payment verified · not 50+ proposals · not
20–50 proposals unless under 60 minutes old · hourly ceiling ≥ $70 · fixed budget ≥ $500 ·
on-thesis.

**Page-only checks** — these cannot fire at harvest; they belong to the verification step and
every survivor gets all four:

- Hours needed above 30/week → out. *"Contract-to-hire" is a full-time role wearing a
  contract label.*
- Client average paid rate below $25/hr → out unless lifetime spend ≥ $10K. Promoted to hard
  §4 on 2026-09-03 after four consecutive cases where it decided the outcome ($15.78 advisor ·
  $9.00 DBA · $16.99 CREST pentest · $15.01 Maropost, bid at $85 and silent since). A client's
  average across dozens of contracts is a settled habit, not noise — it predicted before the
  fact rather than explaining after it.
- Hire rate below 50% → out unless lifetime spend ≥ $10K.
- Bid range shape: a high ceiling with a low average means the ceiling is decoration.

**Every fixed-price candidate is reported with its implied hourly rate** (budget ÷ stated
minimum hours), never the budget alone. Added 2026-09-04 after a $1,111 fractional-CTO job was
reported with its budget but not its ~$18.50/hr, which was the figure that decided it.

---

## Kill rules, all absolute

- **Never-hires trap (6-for-6):** $0 lifetime spend or 0% hire rate kills it however good the
  spec reads. Bench posts are this in disguise.
- **Tool / credential / discipline fluency:** if a job names a platform, credential or
  discipline he does not have, it is out — do not write around it. Killed so far: GoHighLevel,
  Camunda, Zendesk AI, Microsoft Foundry, Laravel, Korean-required, CREST-certified pentest,
  OCI/SAP, vendor-specific GCP/AWS, Retell/Asterisk VoIP, SOC and incident response,
  Axcelerate/Moodle.
- **On-thesis only:** AI agents / LLM / RAG / MCP, architecture review, technical due
  diligence, fractional CTO, rescue of half-finished codebases; TypeScript / Node / Bun /
  Elixir / Clojure.

---

## Angles tested and closed

| Angle | Verdict |
|---|---|
| Rare-tech arbitrage (Elixir, Clojure) | Dead. 2 Elixir jobs and 1 Clojure across the whole period, both bid-swarmed. |
| Language arbitrage (German, Dutch) | Real moat — 70% of German jobs under 15 bids, 24 of 50 Dutch under 5 — but it guards voice recording, UGC, customer support and transcription, not architecture. |
| Badges | None held; not acquirable without history. |
| Availability badge | Costs 14 Connects/week under "Promote with ads". Not free. Cancelled unused. |
| **Infra / DevOps widening (BUCKET-B)** | **Retired 2026-09-04.** See below. |

**BUCKET-B, in full.** Added 2026-09-02 after the observation that 20 sweeps had confined
every bid to the AI-agent pool — measurably the worst-priced corner of the platform (2 of 27
hourly jobs clear $70, against 7 of 22 in DevOps, which also has the highest
payment-verification rate at 46/50). The positioning note lists DevOps as a core pillar and it
had never once been searched.

Ran Sep 2–4, five sweeps, **zero bid-worthy candidates**. The measurement stands — infra does
price better on average — but the listings reachable without vendor certification or a review
history sit in the same commodity tier as the AI pool. Widening bought volume, not
opportunity, and cost ~150 tiles of noise per sweep. Retired on the human's approval.

---

## Loop status

Crons v6, session-only, armed 2026-09-04 at 07:53 and 13:29, expiring ~2026-09-11.
THESIS queries only (8), roughly 300 tiles per run. Zero candidates is the stated expected
outcome, not a failure.

**Watch condition:** if a full week passes with zero candidates, suspect the filter rather
than the market and say so. The rules above make a thin market thinner; the failure mode to
avoid is a channel dying of caution rather than of market reality.
