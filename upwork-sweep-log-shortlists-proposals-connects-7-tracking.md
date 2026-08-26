---
title: 'Upwork Sweep Log — shortlists, proposals, Connects (§7 tracking)'
visibility: restricted
---
# Upwork Sweep Log

Running log for the assisted sweep (P2/P3) of `upwork-plan-fast-income-channel-assisted-human-approved`.
One section per sweep. Feeds the §7 metrics and kill criteria.

**Hard rule carried from §8:** no automated submission, ever. Every send is a human click.

---

## §7 running totals

| Metric | Total to date |
|---|---|
| Proposals sent | 0 |
| Viewed | 0 |
| Replied | 0 |
| Interviews | 0 |
| Contracts | 0 |
| Connects spent | 0 |

Kill criteria: <5 % reply rate after 20 proposals → stop, re-diagnose positioning/rate.
30 proposals, 0 replies → halt and rewrite. First contract by week 3 = on track.

---

## Sweep 1 — 2026-08-26 (first P2 sweep)

**Outcome: no proposals sent.** Chrome was not authenticated to Upwork — `/nx/find-work/`
redirected to the login screen (`work@rizom.ai` prefilled, password pending), and only one
browser was connected, so no other session held the login. Sweep was run against the
logged-out public search instead, which still works and is recency-sortable.

**Connects spent: 0.**

### Coverage

342 unique listings across 8 recency-sorted queries covering the full §4 Prefer surface:
AI agent/agentic · LLM · RAG/vector · MCP/Model Context Protocol · architecture review /
technical due diligence / code audit · fractional CTO / technical advisor · take-over /
rescue / inherited codebase / half-finished · Elixir/Clojure/Bun/TypeScript architect.

- 118 passed the mechanical filter (rate floor, hours/week, topic fit)
- 104 survived a negative filter (SEO/AEO, ads, voiceover, patent, Webflow, Shopify, Zoho, copywriting)
- ranked to 10 on on-profile signal + §4 recency weight

### Filter status — provisional

Applied from public data: hourly max < $70 excluded · fixed-price < $500 excluded ·
"More than 30 hrs/week" excluded · topic fit + negative filter.

**Not verifiable logged out — all four are §4 hard-excludes:** payment method verified ·
existing bid count (>30 rule) · client lifetime spend (>$5k preference) · client hire rate
(<50 %) / 0-hires-with-large-budget. Every row below is provisional until these run on the
logged-in view.

### Ranked shortlist

| # | Job | Posted | Budget | Reasoning |
|---|-----|--------|--------|-----------|
| 1 | [AI Workflow Consolidation & Access-Control Architecture (n8n / Postgres)](https://www.upwork.com/jobs/~022092392982665135086) | 9h | $2.5k fixed | ~100-employee group two months into a build that needs consolidating — architecture + access control, fixed-price, real org with real money; closest thing in the sweep to an architecture-review mandate. |
| 2 | [Senior data/backend engineer to productionise an existing AI extraction pipeline](https://www.upwork.com/jobs/~022092479696706164345) | 3h | $500 fixed | Textbook §4 "rescue of a half-finished codebase" and the freshest serious listing — but $500 sits exactly on the fixed-price floor, so scope must be genuinely small or it is a hard exclude. |
| 3 | [AI Automation architect — build a small workforce for a business](https://www.upwork.com/jobs/~022092455256621458048) | 2h | fixed, undisclosed | Multi-agent "AI workforce" framing maps directly onto brains; posted <4h so the response-speed lever is live, but budget is unstated and must be checked. |
| 4 | [AI Document Search Engine for 500GB + QuickBooks integration (nonprofit)](https://www.upwork.com/jobs/~022092284904638469753) | 1d | $24k fixed | Largest budget in the sweep and squarely RAG-over-private-corpus; 500GB implies real retrieval engineering, not an API wrapper. |
| 5 | [AI Engineer for Knowledge Base & AI System Implementation](https://www.upwork.com/jobs/~022091608253212820462) | 2d | $1.7k fixed | Knowledge-base architecture — the Lefthoek/Rizom proof point maps one-to-one; "architect, implement, deploy, scale" is ownership language, not ticket language. |
| 6 | [Build a policy search app with source citations (Next.js, Supabase, OpenAI)](https://www.upwork.com/jobs/~022091873420404990592) | 2d | hourly, undisclosed | Citation-grounded retrieval is the hard part of RAG and exactly what brains does; TypeScript stack fits the §4 language preference. |
| 7 | [Technical Lead / Solutions Architect](https://www.upwork.com/jobs/~022092005043820987374) | 2d | $150/h | Rate is at the §2 Top-Rated band, well clear of cold start; generic title means the spec detail needs checking against the vague-spec exclude. |
| 8 | [Fractional CTO for Startup](https://www.upwork.com/jobs/~022090782836479825252) | 5d | $150/h | Direct §4 "fractional CTO" hit at a rate that skips the cold-start discount entirely; age means bid count is the deciding check. |
| 9 | [Fractional CTO (Client-Facing) — Senior Software Engineer, Part-Time](https://www.upwork.com/jobs/~022091911816365753721) | 2d | $80/h | Explicitly part-time, which matches the 15–20 h capacity constraint that kills most fractional listings; $80/h is mid cold-start band. |
| 10 | [Fractional Technical Lead / Enterprise Solutions Architect (Texas-Based)](https://www.upwork.com/jobs/~022090993067233842835) | 4d | $1.5k fixed | On-profile fractional-architect scope, but "Texas-Based" in the title is a likely location hard-exclude — verify before spending a Connect. |

### Skipped, and why

- **Principal AI Architect / Fractional CTO Advisor** — perfect topic match, $30–60/h. Below the $70 floor. Hard exclude (§2), no exception for fit.
- **Principal Platform Architect: CRM + Voice AI** ($3.5k) — 14 days old; bid count almost certainly past 30.
- **GEO/AEO Specialist** — "Full Time" contract; fails the 40 h/week exclude against 15–20 h capacity.
- **Multiuser AI Chatbot (Amazon Bedrock AgentCore)** — $40 fixed. Far below floor.
- **Fix Vapi Voice AI Agent for Restaurant** — $50 fixed. Far below floor.
- Remainder of the <4 h band (poultry farm app, Webflow port, freight-forwarding agent) — off-profile.

### Open items surfaced by this sweep

1. **No English profile text exists.** §1 of the plan says to reuse "the English text from `Freelance-Profil`", but `freelance-positioning-dachnl-profil-raten-launch-checkliste` carries only the German and Dutch texts. An English, AI-first profile text still has to be written — it is a P0 dependency, not a P2 one.
2. **P0 approval state unconfirmed.** §6 gates P2 behind profile approval; not verifiable from outside the account.
3. **Recency lever is thin per sweep.** Only 6 of 118 passing listings were posted <4 h. Supports P3's morning loop over a single large daily pass.

### Method note (reusable for P3)

Logged-out public search at `upwork.com/nx/search/jobs/?q=<query>&sort=recency&per_page=50`
returns 50 tiles per page and exposes: posted-age, title, hourly band or fixed budget,
experience level, hours/week, description. It does **not** expose payment-verified, bid
count, client spend or hire rate. So a logged-out pass is useful for building the candidate
pool cheaply, but the §4 hard-excludes always require the authenticated view.
