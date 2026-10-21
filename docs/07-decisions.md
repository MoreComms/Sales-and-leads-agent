# 07 · Decisions

## Decided (21 Oct 2026)

| # | Decision | What we agreed |
|---|---|---|
| D1 | **How plays are prioritised** | **They aren't.** Balanced weekly slate: the 40 new contacts a week are split evenly across P1–P8 (about 5 each). Spare slots go to the strongest waiting leads, never to weak ones. P0 Reactivation runs alongside. P9 and P10 produce alerts, not emails. |
| D2 | **Who sends** | **Charles only, as a case study.** Daniel, Jojo and Elsa join later if the results justify it. |
| D3 | **Autonomy** | Charles sends every first email himself (sending = approving the sequence). The agent sends follow-ups 2 and 3 only if nobody replied. Scheduling replies stay drafts until Charles switches on `auto_scheduling`. |
| D4 | **Sending domain** | **Everything from wedomore.com, no new domains.** Caps of 10 new a day and 40 a week; 3 emails per sequence; automatic pause on bounces. |
| D5 | **What the agent may cite** | Any client or project on the website, freely. Anything else is offered as options in the morning summary for Charles to pick. Prices are never quoted. |
| D6 | **Access** | Charles's Gmail, Calendar, Drive and Sheets, through the connections already set up for his Claude account |
| D7 | **Geography and language** | UAE first, in English. Kuwait and Qatar allowed for agency audio. No cold email to KSA or Germany. |
| D8 | **Legal** | Charles confirmed MORE is fine legally. Opt-outs, source records and data retention stay as good practice. |
| D9 | **Budget** | **$0 extra.** Runs on Charles's Claude plan and MORE's Google Workspace. Optional email verification (~$5–10/month) later, if needed. |
| D10 | **Build** | **The lightweight build, long term.** Scheduled Claude sessions, this repo for instructions, a Google Sheet for memory, Gmail drafts for review. No dashboard, servers or paid tools (see 04). |
| D11 | **Alerts** | By email to Charles |
| D15 | **Ramadan target list** | The 43 brands in [08](08-ramadan-target-brands.md), approved as they are |
| D20 | **Ramadan boost** | None. P5 keeps its normal share. |
| D21 | **Sponsorship** | No sponsorship pitching. P5 pitches branded entertainment and Ramadan content the brand owns. |
| D22 | **Incoming requests** | The agent watches knowmore@ (which lands in Charles's inbox) and the website form, and drafts replies with studio-room availability |

## Setup status

| Step | Status |
|---|---|
| Agent instructions (`CLAUDE.md`, `agent/jobs/`) and settings (`config/`) | ✅ Done |
| Voice guide from Charles's own emails (`config/voice-charles.md`) | ✅ Done |
| **MORE Sales Agent** sheet in Charles's Drive, with all tabs and Settings | ✅ Done |
| Gmail labels | ⚠️ Google refused label creation through the connector. Optional: Charles can create `MORE Agent/To review`, `MORE Agent/Live` and `MORE Agent/Summaries` himself. The agent works without them. |
| First batch of drafts in Charles's Gmail | In progress |
| Schedules switched on | After Charles reviews the first batch |

## Questions for Charles

| # | Question | Default if no answer |
|---|---|---|
| Q1 | **Is the new website live?** The copy review said it was still staged in Webflow on 11 Oct. | `site_live = no`: no page links, and no "we've relaunched" line |
| Q2 | **Which deck or profile link may drafts include**, if any: https://more-2026.figma.site/ or none? | No deck link; website only, once live |
| Q3 | Spelling: your emails mix -ize and -ise. Pick one for drafts? | Follow your habit (mostly -ize), consistent within each email |
| Q4 | Should the Workspace admin confirm wedomore.com's SPF, DKIM and DMARC records? It takes about 5 minutes, and protects deliverability. | Recommended |
| Q5 | Forward tender portal alert emails to your inbox, if they go elsewhere? | Agent searches your inbox for tender alerts only |

## Can be settled later

| # | Decision | Recommendation |
|---|---|---|
| D12 | Write-back to MORE – CRM | Off for the first weeks; then let the agent update Charles's own rows |
| D14 | Value-first assets | Voice shortlists (P1) need the audio team's reels tagged by dialect. Format one-pagers (P5) are prepared after interest. |
| D18 | Investors and creators | Investors stay fully manual. Creators (P10) are suggestions in the Friday report only. |
| D19 | Market context | Confirm the 2026 downturn reading in 02 and the 2027 watchlist |
