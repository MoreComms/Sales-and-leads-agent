# 06 · Roadmap, metrics and costs

Dates assume we agree the plan this week. Ramadan 2027 is expected around 8 February, which makes **15 November – mid December the sponsorship selling window**. The roadmap is built around hitting it.

## Phases

### Week 0 · Decide and set up (21 Oct – 31 Oct)
- Agree the decisions in [07-decisions.md](07-decisions.md).
- **Buy the secondary domains and start inbox warm-up (2–3 weeks of lead time).**
- Register or confirm vendor accounts on Tahweel (Dubai Holding), Dubai eSupply, ADGPG and the federal Digital Procurement Platform, and route their alert emails to one inbox.
- Book the UAE counsel review on cold B2B email under the PDPL.
- Charles approves the **proof list** (nameable clients) and **price rules**.
- Each sender opts in: Gmail read access for reactivation and voice learning, and calendar access for scheduling.
- Collect assets: the current deck link, showreel, studio walkthrough, tagged voice reels, and the slate one-liners that can be shared.

### Phase 1 · Foundation and warm plays (3 Nov – 21 Nov)
- Database, worker, dashboard v1 (review queue), audit log, kill switch.
- Import and dedupe **MORE – CRM**; add play, agent status, thread link and opt-out columns; switch on two-way sync.
- Gmail, Calendar and Sheets integrations; researcher, writer and critic; sender voice guides drafted and approved.
- **P0 Reactivation live at L1:** drafts land in each sender's Gmail, starting with the ledger's past clients.
- **P5 Ramadan sprint, concierge mode, from ~10 Nov:** research dossiers, show-fit notes and first-touch drafts for an agreed list of ~40 target brands, ready for Charles and Daniel by **15 Nov**.
- Reply triage v1: classify and draft; humans send.

### Phase 2 · Signals and cold plays (24 Nov – 19 Dec)
- Signal collectors: agency news (account wins and moves), the tender alert inbox, podcast launches, film-commission news.
- Contact-data vendor pilot on 300 known contacts, then the email waterfall and verification go live.
- Cold sending on the warmed domains; sequences, follow-ups and stop rules.
- Scheduling from owners' calendars, studio-visit invites, prep briefs.
- **P1 Agency audio and P7 Studios live at L2. P9 Tender radar live (L0).**
- Weekly report v1, per play.

### Phase 3 · Expand and learn (January 2027)
- **Pre-Ramadan push on P1 and P2:** Ramadan production briefs peak.
- P3 Studio-to-studio, P2 Agency production, P4 Brand sound.
- LinkedIn task queue (human-sent); WhatsApp one-tap drafts and opt-in flow.
- Learning loop: weekly edit-pattern summaries leading to proposed template changes.
- First graduations to L3 for plays that earn it; Arabic drafts with native review.

### Phase 4 · Ramadan and beyond (February 2027 on)
- During Ramadan: greetings and nurture only, no new cold sequences; meetings and proposals continue.
- After Eid: P8 Artist services (once pricing is validated), P6 Challenger brands, P10 Creators.
- KSA outreach plan after counsel and SDAIA's final rules.
- CRM review: keep the sheet, or move the pipeline to ClickUp or HubSpot.

## How we'll measure it

| Kind | Metric | Initial target [est., recalibrated after 4 weeks of data] |
|---|---|---|
| Quality | Draft approval rate with light or no edits | ≥80% by end of Phase 1, ≥90% to graduate a play |
| Quality | Untraceable claims reaching a human | 0 |
| Outcome | **Reply rate, P0 Reactivation** | 25–40% |
| Outcome | **Reply rate, Tier A signal sends** | 8–15% |
| Outcome | Reply rate, Tier B | 4–8% |
| Outcome | Contacted accounts that book a meeting (signal plays) | 2–4% |
| Outcome | Meetings booked and held, opportunities created, AED pipeline, won revenue: per play, per owner | Baseline in Phase 1 |
| Health | Bounce rate | <2% |
| Health | Spam complaints | <0.1% |
| Health | Unsubscribe rate | <1% per send |
| Team | Time spent reviewing | ~15 minutes a day per owner |

Illustrative month once Phases 1 and 2 are running: ~200 reactivations plus ~300 new signal contacts could yield **roughly 15–30 meetings [est.]**. Most of them come from reactivation at first, shifting to signal plays as reactivation is worked through. Real numbers replace this estimate after the first four weeks.

## Running costs (USD per month, excluding build time)

| Item | Phase 1 (warm only) | ~500 prospects/mo | ~1,500 prospects/mo |
|---|---|---|---|
| Database, worker, hosting (Supabase, Trigger.dev, Cloud Run) | ~45 | ~45 | ~105 |
| Claude API (Opus 5.5: research, writing, checking, replies; caching + Batch where possible) [est.] | 100–200 | 250–450 | 700–1,200 |
| Cold sending platform (Instantly; warm-up from week 0) | 37–97 | 97 | 97 |
| Secondary domains + Workspace inboxes | ~50 | ~50 | ~130 |
| Contact data + verification (Apollo, Prospeo, Findymail, MillionVerifier) | — | ~160 | ~310 |
| Signals (TheirStack, Apify; news, tenders and podcasts are free) | — | ~90 | ~160 |
| WhatsApp (after opt-in only) | — | ~5 | ~15 |
| **Total [est.]** | **~$230–390** | **~$700–900** | **~$1,500–2,000** |

For comparison, AI-SDR SaaS runs from about $900/month (AiSDR, capped at 1,200 messages) to about $3,750/month (11x), without MORE's voice, Gulf data or approval gate. Annual billing takes 15–20% off most tool lines. Re-check every vendor price at signup; these are October 2026 third-party figures.

## Risks and mitigations

| Risk | Mitigation |
|---|---|
| Gulf contact data is patchy and goes stale | Vendor pilot before buying; waterfall + verification; LinkedIn fallback; warm-first |
| Deliverability damage | Never cold from wedomore.com; warm-up; caps; plain text; automatic kill switch |
| Legal exposure (UAE/KSA PDPL) | Counsel review before cold plays; UAE-first; no cold KSA at launch; instant opt-out; source records |
| An AI-sounding or wrong message hurts the brand | Human approval until graduation; claim tracing; critic; voice guides from real sent mail |
| Owners don't have time to review | Mobile review queue, Gmail drafts, batch approve, ~15 minutes a day; volume matched to review capacity |
| The 2026 market downturn | Lead with cheaper and faster offers; government entertainment and tourism focus; real estate and hotels on a 2027 watchlist |
| Relationship culture resists cold outreach | Warm-first, studio visits as the default ask, WhatsApp and phone only from humans |
| Vendor lock-in | MORE owns its domains, inboxes and data; every vendor has a fallback |
