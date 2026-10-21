# 07 · Decisions

## Decided (21 Oct 2026)

| # | Decision | What we agreed |
|---|---|---|
| D1 | **How plays are prioritised** | **They aren't.** Balanced weekly slate: the 40 new contacts a week are split evenly across P1–P8 (about 5 each). Spare slots go to the strongest waiting leads, never to weak ones. P0 Reactivation runs alongside as warm drafts. P9 and P10 produce alerts, not emails. |
| D2 | **Who sends** | **Charles only, as a case study.** Daniel, Jojo and Elsa join later if the results justify it. |
| D4 | **Sending domain** | **Everything from wedomore.com, no new domains.** Hand-picked high-potential leads only; caps of 10 new a day and 40 a week; 3 emails per sequence at most; automatic pause on reputation trouble. |
| D5 | **What the agent may cite** | Any client or project on the website, freely. Anything else is offered as 2–3 personalisation options for Charles to pick in the review queue. Prices are never quoted in outreach; price questions go to Charles. |
| D6 | **Access** | Charles opts in to Gmail (read for reactivation and voice, draft and send for his approved emails) and Calendar (free/busy and booking). Granted when we start building. |
| D7 | **Geography and language** | UAE first, in English. No cold email to KSA at launch (warm intros and human-sent LinkedIn only). International only for P3 studio-to-studio, never Germany. |
| D8 | **Legal** | Charles confirmed MORE is fine legally. Opt-outs, source records and data retention stay in place as good practice. |
| D11 | **Alerts** | By email to Charles: drafts ready, hot replies, meetings booked, new RFQs. |
| D15 | **Ramadan target list** | The 43 brands in [08](08-ramadan-target-brands.md) are approved as they are. |
| D20 | **Ramadan boost** | None. P5 keeps its normal share of the balanced slate. |
| D21 | **Sponsorship** | **No sponsorship pitching for now.** The Rahal Show hasn't launched. P5 pitches branded entertainment and Ramadan content that the brand owns; MORE Originals aren't pitched until a show launches. |
| D3 | **Autonomy** | Charles approves every first touch, permanently. Follow-ups go out automatically within a sequence he approved, unless the contact replies. Reactivation drafts land in his Gmail for him to send. Scheduling replies can become automatic later, once earned. |
| D22 | **Incoming requests** | The agent watches knowmore@wedomore.com and the website contact form, and drafts replies to incoming studio and brief requests for Charles. |

## Last two before we build

| # | Decision | Recommendation |
|---|---|---|
| **D9** | **Budget** | ~$145–245/month for Phase 1, ~$360–700/month at steady state (see 06), with spend caps per play |
| **D10** | **Stack** | TypeScript; Trigger.dev; Supabase; Google Cloud Run; Claude API; Gmail API from Charles's mailbox; Apollo → Findymail + MillionVerifier; Google Calendar; the MORE – CRM sheet kept as the team view |

## What's needed from MORE to start building

1. **Anthropic API key** for a MORE workspace, with a monthly spend limit.
2. **Google Workspace:**
   - Approve the agent's sign-in for Charles's Gmail and Calendar.
   - Delegate access to knowmore@wedomore.com.
   - Share the MORE – CRM sheet with the agent's service account.
   - Confirm SPF, DKIM and DMARC on wedomore.com (the Workspace admin can check in minutes).
3. **Accounts on a MORE card:** Google Cloud project, Supabase, Trigger.dev, Apollo, Findymail, MillionVerifier. The setup steps will be provided; nothing is bought without your go-ahead.
4. **Tender portals:** forward the alert emails from Tahweel, Dubai eSupply, ADGPG and the federal platform to one inbox the agent can read.

## Can be settled during Phase 1

| # | Decision | Recommendation |
|---|---|---|
| D12 | CRM long term | Keep the sheet through the case study, then decide between ClickUp (already used for production) and HubSpot Free |
| D13 | Model choice | Claude Opus 5.5 for every step at launch. After a month of usage data, Charles decides whether cheaper models should handle the high-volume classification steps. |
| D14 | Value-first assets | The voice shortlists for P1 need the roster's voice reels tagged by dialect and tone, probably by the audio team. Agree who does that, and approve the other hooks (sonic audit, format one-pager, studio walkthrough). |
| D16 | Signature | Charles's existing Gmail signature is used as-is, unless he wants a different one for outreach |
| D17 | Deck link | The new website pages per door, or https://more-2026.figma.site/? |
| D18 | Investors and creators | Investors stay fully manual. Creators (P10) are suggestions only; Instagram DMs stay human. |
| D19 | Market context | Confirm the 2026 downturn reading in 02, and whether real estate and hotel pre-openings stay on the 2027 watchlist |
