# 02 · Lead sourcing: where leads come from, and how the agent knows "now"

## The principle: warm first, then signals, never static lists

The data is consistent. Cold email averages a **3–4.5% reply rate** in 2025–26 (Instantly, Hunter). Small, time-bound groups do far better than big lists: 6.2% replies at 21–50 recipients against 2.4% at 500+. Accounts with an active trigger close at roughly twice the rate of accounts without one.

The GCC adds a relationship-first culture, where a cold email as the first touch does worse than in North America. So the agent sources in this order:

1. **Warm: people who already know MORE.** Past clients, dormant contacts, people met and pitched to. Highest reply rate, lowest risk, and the new website is the reason to reconnect.
2. **Signals: an event that creates a need right now.** An agency wins an account, a brand announces a sponsorship, an RFQ drops, a podcast launches, a production is announced for the UAE.
3. **Lists only to fill gaps,** and only inside a play, filtered by fit and refreshed against signals. No generic "UAE marketing directors" blasts.

## 2026 context: what it changes (please confirm)

Our market research picked up reports of a regional conflict affecting the Gulf economy through 2026:
- The IMF's October outlook has UAE and KSA GDP contracting in 2026 and rebounding strongly in 2027.
- DXB traffic fell sharply in Q1.
- WARC cut its Gulf ad-spend forecast.
- AGBI reported agency job cuts in July.
- Dubai announced an AED 2.5bn tourism and entertainment support package.

**You'll know better than any search result how accurate this is.** If it holds, the plan adapts as follows:

- **Lead with cheaper, faster, easy-to-justify offers through Q1 2027:** audio and VO, Arabic adaptation of global campaigns, content retainers, studio time. This is P1, P3 and P7.
- **Government and semi-government entertainment and tourism budgets become the steadiest money:** DHE, DET, DCT, GEA/Riyadh Season. P9 (tender radar) and relationship-led work move up.
- **Agencies cutting in-house teams may outsource more,** which favours P1 and P2. This is our inference, not verified.
- **Hotel pre-openings and off-plan real-estate launches go on a "2027 rebound watchlist"** rather than being launch targets.

## Source 1: internal and warm data (start here)

| Source | What we get | Est. size | Notes |
|---|---|---|---|
| **MORE – CRM** sheet | Local Production & Brands (~71), International Clients (~110), UAE Brands (~118), UAE Talents (75) | ~370 rows | Duplicates across tabs, missing emails, no opt-out field. The agent imports, dedupes and normalises it once. |
| **2024–26 sales ledger** | Every paying client: Craft, Translate Plus, NOVAE, McCann, Memac Ogilvy, Berklee, Emaar, Deliveroo, SRMG, Pure Health, Wego, Etihad and more | ~100+ accounts [est.] | Best reactivation list: they've paid us before |
| **Gmail history** of Charles, Daniel, Jojo and Elsa (read-only, opt-in per person) | People we've emailed with in the last ~5 years who've gone quiet for 6+ months; also the sender's real writing voice | Hundreds [est.] | Needs each person's consent; see decisions |
| **Drive prospect lists** | *Kitchen Studio Clients to approach*, *Podcast Studio Clients To approach* | Dozens | Ready-made P7 targets |
| **Meeting notes** (Gemini notes in Drive) | People met and pitched to, follow-ups promised and not done | — | Turns into reactivation tasks |
| **Event and award credits** | Dubai Lynx 2026 winners and credits (8 Oct), Effie MENA shortlists | — | A fresh map of active agency producers |

## Source 2: signals, mapped to plays

Ranked by how well a correctly timed contact converts, and how hard it is to detect automatically.

| # | Signal | Play | Where the agent watches | Cost | Detection |
|---|---|---|---|---|---|
| 1 | **Agency account win or new AOR**: first flights need dialect VO, music and a fast mix within 30–90 days | P1, P2 | Campaign ME, Communicate, Arabian Marketer, ArabAd, LBB (RSS) + Claude classification | Free | Easy |
| 2 | **Entertainment or tourism RFQ/tender** | P9 | Alert emails from Tahweel (Dubai Holding), Dubai eSupply, ADGPG, federal DPP, Etimad, routed to a dedicated inbox the agent reads | Free (registration needed) | Medium |
| 3 | **Ramadan 2027 window** (Ramadan expected ~8 Feb 2027; budgets lock Oct–Jan) | P5, P1, P2 | Calendar trigger + last year's Ramadan advertisers and series sponsors | Free | Easy |
| 4 | **Brand sponsorship or content-partnership announcement** | P5, P4 | Zawya, WAM, Dubai Media Office, Google News RSS, GDELT | Free | Easy–medium |
| 5 | **New CMO, head of partnerships or head of content** (first 90 days = roster review) | P5, P4, P2 | Press appointment notices; Apollo job-change data; Sales Navigator alerts (human-checked) | Included in Apollo | Medium |
| 6 | **International shoot announced for UAE/KSA** (Abu Dhabi rebate 35–50%, Saudi up to 60%) | P3 | Abu Dhabi Film Commission/CMA and Saudi Film Commission news, KFTV, Screen, Variety/Deadline | Free | Medium |
| 7 | **Streamer or broadcaster commissioning** (MBC/Shahid, OSN+, Netflix MENA, Thmanyah) | P3 (dubbing, Atmos), Originals | BroadcastPro ME, Señal News, slate announcements; DICM in November | Free | Medium (low volume; human judgement) |
| 8 | **New podcast or creator channel in UAE/KSA** | P7, P10 | Apple Podcasts search API (store ae/sa), Podcast Index, YouTube Data API | Free | Easy |
| 9 | **Brand entering UAE/KSA, or a global campaign with no Arabic version** | P1, P4 | Press releases, KSA regional-HQ moves, regional YouTube | Free | Medium |
| 10 | **Artist release or tour through Dubai** | P8 | Anghami/Apple charts, label news (Spotify's API is now restricted) | Free / paid Chartmetric later | Medium |
| 11 | **F&B opening or expansion** | P7 (kitchen studio), P6 | Openings coverage (Time Out Dubai, What's On), developer and mall news | Free | Medium |
| 12 | **Job post for in-house producer or editor** (capacity gap) | P2, retainers | TheirStack (GCC coverage unverified) | ~$59/mo | Medium |
| 13 | **Funding round, Series A+ consumer brands only** | P6, P4 | Wamda, MAGNiTT summaries | Free | Easy (low priority) |

**Dropped signals:** outdated websites, app launches, web performance. Those were digital-agency triggers and are no longer MORE's business. Ad-library monitoring is a research input, not a trigger: Meta's API excludes UAE/KSA commercial ads, and scraping breaks its terms.

## Source 3: finding the right person

For every account that clears scoring, the agent finds the buyer titles the play defines (for example P1: *Head of Production, Producer, TV/Radio Producer, Integrated Producer*):

1. **Search:** Apollo People Search (free with a master API key; returns names, titles and LinkedIn URLs, no emails).
2. **Email waterfall:** Apollo enrichment, then Prospeo, then Findymail (pay only for verified finds).
3. **Verification:** MillionVerifier on every address. Catch-all domains are only used for Tier A accounts, and only after a small pilot.
4. **Gaps:** if no verified email is found, the contact goes to a LinkedIn task for a human.

Expect a lower find rate than in the US: **about 50–65% verified [est.]**. Expat turnover makes data go stale fast. **Before committing to vendors, we run 300 known UAE/KSA contacts (from the CRM and ledger) through 3–4 providers** and pick on measured fill and bounce rates.

## Scoring: who gets researched, who gets a hand-made asset

Every candidate gets three scores. Claude judges them against the play's rubric, with structured output so they're auditable.

- **Fit (0–5):** does the account match the play's buyer, size and category? Is this the right person?
- **Timing (0–5):** how strong and how recent is the signal? Decays over 0–30 days. Inside the Ramadan window counts.
- **Value (0–5):** likely deal size and strategic value (e.g. a sponsor for an Original scores above a one-off VO spot).

| Tier | Rule (initial, to tune) | What happens |
|---|---|---|
| **A** | High on all three | Deep research, partner-level draft, often a value-first asset; owner reviews every word |
| **B** | Good fit, a real signal | Standard research, play template, human approval |
| **C** | Fit but no timing | Nurture list; re-scored when a new signal appears |
| **Out** | Poor fit, on the suppression list, already in an open conversation with someone at MORE, or a protected contact (Sheikhs, Excellencies, investors) | Never contacted by the agent |

**Collision rule:** if anyone at MORE has emailed the contact in the last 90 days, or the CRM shows an owner and an active stage, the agent does not start a sequence. It surfaces the signal to that owner instead ("Omar's agency just won X, worth a note?").

## Volumes we're planning for (to confirm)

- **Reactivation (P0):** 150–300 people in the first month, then a steady trickle as relationships go quiet.
- **New contacts across signal plays:** ~300 a month to start, up to ~1,000 once plays are tuned. Quality over volume.
- **Tender radar:** every relevant RFQ, no outreach.
