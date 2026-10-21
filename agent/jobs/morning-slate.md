# Job: morning slate (Mon–Fri, 07:45 Dubai)

**Goal:** leave Charles a small set of excellent drafts to review, balanced across plays, plus a summary email telling him what's there and why.

Read first: `CLAUDE.md`, `config/guardrails.md`, `config/plays.md`, `config/proof.md`, `config/voice-charles.md`, `config/sheet.md`.

## 0. Should I run?

- Stop quietly if any of these is true:
  - Settings `paused = yes`;
  - today is Saturday or Sunday;
  - today is on the UAE holidays calendar.
- During Ramadan, skip steps 3–6 for new contacts. Still do reactivations and the summary.

## 1. Load state

- Read the Settings, Leads, Sequences, Signals and Suppression tabs.
- Count the new first-touch drafts created this week (Monday–today, plays P1–P8) and today.
- Count unsent agent drafts: drafts labelled `MORE Agent/To review`.
- **Today's new-draft target:**
  - 8 by default, never above `daily_new_cap`;
  - never above what's left of `weekly_new_cap`;
  - halved if more than 15 drafts are waiting unsent.

## 2. Balance the slate

- Each active play in P1–P8 has a weekly quota: 40 ÷ number of active plays (normally 5), plus any boost in Settings.
- Pick plays in order of most quota remaining this week. Aim for no more than 2 drafts from the same play today unless others have no qualified leads.
- If a play has no qualified lead today, give its slot to the strongest qualified lead from another play. Never lower the bar to fill a slot.

## 3. Find candidates for each chosen play

In this order:
1. Unused signals in the Signals tab from the last 14 days for that play, strongest first.
2. For P5: brands in `docs/08-ramadan-target-brands.md` not yet in Leads (warm ★ brands are P0, not P5).
3. For P7: the Drive prospect lists in `config/sources.md`.
4. For P1/P2: CRM rows (Local Production & Brands) with no owner, or led by Charles and quiet since June.
5. Fresh web research using `config/sources.md`.

## 4. Check each candidate before spending effort

Skip and record the reason in Leads (Status `skipped`) if any of these is true:
- the address or domain is in Suppression;
- the collision check fails (see `config/guardrails.md`);
- the only address is personal;
- the target is in Saudi Arabia or Germany;
- the person is protected;
- the fit is weak.

## 5. Score, find the person, research

- Score Fit, Timing and Value (0–5).
- Keep only **Tier A** (strong on all three) or **Tier B with a signal from the last 14 days**. Everything else goes to Leads as `nurture`.
- Find the right person by the play's buyer titles: CRM, Charles's Gmail, the company's website or team page, press releases.
- If you can't find a work email you're confident in, save the lead as `linkedin-it`, with the person's name and LinkedIn URL if found, and no draft.
- Research: 3–6 facts with their URLs (the signal in context, what they're working on, anything that makes the email specific). Save them in Research.

## 6. Write and create the draft

1. Write email 1 using the play's shape, Charles's voice and the guardrails. Pick the most relevant *free to name* receipt from `config/proof.md`, if any.
2. If an *options only* receipt or a different angle would be clearly better, don't use it. Write it as an option for the summary (e.g. `3B: mention the Samsung spot mixed with Craft`) and save it in Options offered.
3. Write follow-ups 2 and 3 and add them to Sequences with Status `waiting-for-email-1`.
4. **Self-check against `config/guardrails.md` before creating anything:**
   - every fact sourced;
   - under 100 words;
   - one ask, at most one link;
   - no banned phrases;
   - no price;
   - receipt allowed;
   - recipient not suppressed;
   - work address.

   Fix anything that fails. If it still fails, don't create the draft; note it in Leads.
5. Create the Gmail draft: to the contact, your subject, plain-text body, `includeSignature: true`. Label its thread `MORE Agent/To review`.
6. Update the Leads row: Status `drafted`, Draft ID, Options offered. Log it.

## 7. Reactivations (P0), up to `daily_reactivation_cap`

- Take `queued` P0 rows from Leads, best first.
- Re-check that the thread is still dormant: no email with them in the last 60 days.
- Write a short personal note per `config/plays.md` → P0 and create the draft as in step 6. P0 sequences have one gentle nudge only, after 10 working days.

## 8. Morning summary email to Charles

- Send to charles@wedomore.com and label it `MORE Agent/Summaries`.
- **Subject:** `MORE Agent · [Day DD Mon] · [N] drafts ready`
- **Body:** plain text, short. Sections:
  - **Ready to review:** numbered list. For each: name, company, play, the one-line reason now, and the Gmail draft link.
  - **Options:** for any draft with alternatives, e.g. `3A (current): FoodTok · 3B: Samsung spot via Craft`. End with "Reply with picks like 3B, or 'skip 4'."
  - **LinkedIn it:** people worth contacting with no email found: name, company, LinkedIn link, one-line reason, and a ready-to-paste LinkedIn message for each. Write it in Charles's voice, under 300 characters so it fits a LinkedIn connection note, same sourcing and proof rules as an email, no link unless the play's link fits, and no "Best," sign-off. Save the message in the lead's Notes too.
  - **Still waiting:** drafts older than 3 working days, unsent.
  - **Worth knowing:** up to 3 notable signals, including colleague collisions to pass on.
- Log the summary.
