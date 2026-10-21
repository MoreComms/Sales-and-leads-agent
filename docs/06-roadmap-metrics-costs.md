# 06 · Roadmap, metrics and costs

Dates assume we agree the plan this week. Ramadan 2027 is expected around 8 February, which makes **15 November – mid December the sponsorship selling window**. The roadmap is built around hitting it.

## Phases

### Week 0 · Decide and set up (21 Oct – 31 Oct)
- Agree the decisions in [07-decisions.md](07-decisions.md).
- **Check wedomore.com's email authentication** (SPF, DKIM, DMARC) and set up Google Postmaster Tools. No new domains are needed.
- Register or confirm vendor accounts on Tahweel (Dubai Holding), Dubai eSupply, ADGPG and the federal Digital Procurement Platform, and route their alert emails to one inbox.
- Charles approves the Ramadan target list ([08](08-ramadan-target-brands.md)) and confirms who sells the Rahal Show inventory.
- Charles opts in: Gmail read access for reactivation and voice learning, and calendar access for scheduling. He is the only sender for the case study.
- Collect assets: the current deck link, showreel, studio walkthrough, tagged voice reels, and the slate one-liners that can be shared.

### Phase 1 · Foundation and warm plays (3 Nov – 21 Nov)
- Database, worker, dashboard v1 (review queue), audit log, kill switch.
- Import and dedupe **MORE – CRM**; add play, agent status, thread link and opt-out columns; switch on two-way sync.
- Gmail, Calendar and Sheets integrations; researcher, writer and critic; sender voice guides drafted and approved.
- **P0 Reactivation live at L1:** drafts land in each sender's Gmail, starting with the ledger's past clients.
- **P5 Ramadan sprint, concierge mode, from ~10 Nov:** research dossiers, show-fit notes and first-touch drafts for the approved brands in [08](08-ramadan-target-brands.md), ready for Charles by **15 Nov**. This is a deadline, not a priority: the Ramadan window closes mid-December.
- Reply triage v1: classify and draft; humans send.

### Phase 2 · Signals and targeted new contacts (24 Nov – 19 Dec)
- Signal collectors: agency news (account wins and moves), the tender alert inbox, podcast launches, film-commission news.
- Contact-data vendor pilot on 300 known contacts, then the email waterfall and verification go live.
- Approved sequences sent from Charles's wedomore.com mailbox, with caps, pacing, follow-ups and stop rules.
- Scheduling from Charles's calendar, studio-visit invites, prep briefs; incoming studio and brief requests triaged to Charles.
- **The balanced weekly slate goes live:** P1–P8 share the 40 new contacts a week evenly (about 5 each). P9 Tender radar live (L0).
- Weekly report v1, per play.

### Phase 3 · Expand and learn (January 2027)
- Ramadan production season: agency signals spike, and the balanced slate absorbs them automatically by moving spare slots to the strongest leads.
- P10 Creator sourcing (suggestions for Charles; Instagram DMs stay human).
- LinkedIn task queue (human-sent); WhatsApp one-tap drafts and opt-in flow.
- Learning loop: weekly edit-pattern summaries leading to proposed template changes.
- Plays that earn it move up a level (drafts → approved sequences → automatic scheduling replies); Arabic drafts with native review.

### Phase 4 · Ramadan and beyond (February 2027 on)
- During Ramadan: greetings and nurture only, no new sequences to new contacts; meetings and proposals continue.
- After Eid: review the case study's results with Charles and decide whether Daniel, Jojo or Elsa join as senders, which raises the weekly cap.
- KSA outreach plan once SDAIA's final rules are out.
- CRM review: keep the sheet, or move the pipeline to ClickUp or HubSpot.

## How we'll measure it

| Kind | Metric | Initial target [est., recalibrated after 4 weeks of data] |
|---|---|---|
| Quality | Draft approval rate with light or no edits | ≥80% by end of Phase 1, ≥90% to graduate a play |
| Quality | Untraceable claims reaching a human | 0 |
| Outcome | **Reply rate, P0 Reactivation** | 25–40% |
| Outcome | **Reply rate, Tier A signal sends** | 10–20% (higher than typical cold email because only hand-picked leads are contacted) |
| Outcome | Reply rate, Tier B with a fresh signal | 6–10% |
| Outcome | Contacted accounts that book a meeting (signal plays) | 3–6% |
| Outcome | Meetings booked and held, opportunities created, AED pipeline, won revenue: per play, per owner | Baseline in Phase 1 |
| Health | Bounce rate | <2% |
| Health | Spam complaints | <0.1% |
| Health | Unsubscribe rate | <1% per send |
| Team | Time Charles spends reviewing | ~20 minutes a day (about 8 new drafts plus reactivation drafts and replies) |

Illustrative month once Phases 1 and 2 are running: ~200 reactivations plus ~150 hand-picked new contacts could yield **roughly 15–25 meetings [est.]**. Most of them come from reactivation at first, shifting to signal plays as reactivation is worked through. Real numbers replace this estimate after the first four weeks.

## Running costs (USD per month, excluding build time)

No sending platform, extra domains or extra inboxes. Everything goes through the Google Workspace mailboxes MORE already pays for.

| Item | Phase 1 (warm only) | Steady state (~150–250 new contacts/mo + reactivation) |
|---|---|---|
| Database, worker, hosting (Supabase, Trigger.dev, Cloud Run) | ~45 | ~45 |
| Claude API (Opus 5.5: research, writing, checking, replies; caching + Batch where possible) [est.] | 100–200 | 200–400 (fewer leads, deeper research per lead) |
| Contact data + verification (Apollo, Findymail, MillionVerifier; Prospeo optional) | — | ~110–160 |
| Signals (TheirStack, Apify optional; news, tenders and podcasts are free) | — | 0–90 |
| WhatsApp (after opt-in only) | — | ~5 |
| **Total [est.]** | **~$145–245** | **~$360–700** |

For comparison, AI-SDR SaaS runs from about $900/month (AiSDR, capped at 1,200 messages) to about $3,750/month (11x), without MORE's voice, Gulf data or approval gate. Annual billing takes 15–20% off most tool lines. Re-check every vendor price at signup; these are October 2026 third-party figures.

## Risks and mitigations

| Risk | Mitigation |
|---|---|
| Gulf contact data is patchy and goes stale | Vendor pilot before buying; waterfall + verification; LinkedIn fallback; warm-first |
| Damage to wedomore.com's sender reputation (it carries all client email too) | Hand-picked leads only; per-sender caps (10 new a day, 40 a week); verification; plain text; Postmaster Tools monitoring; automatic kill switch |
| Legal exposure (UAE/KSA PDPL) | Charles has confirmed the legal position; UAE-first; no cold KSA at launch; instant opt-out; source records kept for every contact |
| An AI-sounding or wrong message hurts the brand | A human approves every first touch; claim tracing; critic; voice guides from real sent mail |
| Owners don't have time to review | Mobile review queue, Gmail drafts, batch approve, ~15 minutes a day; volume matched to review capacity |
| The 2026 market downturn | Lead with cheaper and faster offers; government entertainment and tourism focus; real estate and hotels on a 2027 watchlist |
| Relationship culture resists cold outreach | Warm-first, studio visits as the default ask, WhatsApp and phone only from humans |
| Vendor lock-in | Sending stays in MORE's own Google Workspace; the data lives in MORE's database; every vendor has a fallback |
