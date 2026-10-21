# Job: inbox check (Mon–Fri, hourly 09:00–18:00 Dubai)

**Goal:** nothing waits. Read what came in since the last check, prepare the right response, keep sequences moving, and tell Charles about anything hot.

Read first: `CLAUDE.md`, `config/guardrails.md`, `config/voice-charles.md`, `config/sheet.md`.

## 0. Should I run?

- Stop if Settings `paused = yes`, or if it's Saturday or Sunday.
- On UAE public holidays, still read and classify, but don't send follow-ups.
- Window: from `last_inbox_check` (or 2 hours ago if empty) to now.

## 1. First emails Charles has sent (approval = sending)

- For every Leads row with Status `drafted`, check whether the draft was sent: the draft is gone, and the thread has a message from charles@wedomore.com in Sent.
- If sent:
  - set Status `sent` and fill Thread ID;
  - relabel the thread from `MORE Agent/To review` to `MORE Agent/Live`;
  - in Sequences, set step 2 to `scheduled` with a due date 5–7 working days after the send date.
- Compare the sent text with what you drafted. If Charles changed it meaningfully, add a one-line note to the Log (`edit: …`). The weekly report uses these.
- If a draft was deleted without being sent, set Status `skipped` (Skip reason `Charles deleted`) and cancel its sequence.

## 2. Replies in agent threads

For each new message from someone else in a thread recorded in Leads (Thread ID), read the whole thread, classify the reply and act:

| Reply | What you do |
|---|---|
| **Wants to meet** | Cancel pending follow-ups. Find 3 slots in the next 10 working days with Google Calendar `suggest_time` on charles@wedomore.com: 30 minutes, 10:00–17:00 Dubai, Mon–Thu preferred, never Friday afternoon. Draft a reply in the thread offering the slots, or a studio visit if they're in the UAE. Status `replied-positive`. **Alert Charles now.** If `auto_scheduling = on` and they accepted a specific time, create the event on his calendar (Google Meet, or the studio address) and draft the confirmation. |
| **Interested, wants info** (reel, deck, examples) | Cancel follow-ups. Draft a short reply with the relevant link from `config/proof.md`. If they ask about price, write "pricing question, your call" in the alert instead of answering. Status `replied-positive`. Alert Charles. |
| **Referral** ("talk to X") | Cancel follow-ups. Add the new person to Leads (same play, Status `queued`, note "referred by …"). Draft a thank-you reply. Alert Charles. |
| **Not now** ("after Ramadan", "next quarter") | Cancel follow-ups. Draft a brief thanks. Set Status `nurture` and Next date to what they implied. |
| **Not interested** | Cancel follow-ups. Draft a gracious one-line close (optional). Status `replied-negative`. |
| **Unsubscribe / "stop" / "remove me" / "where did you get my email"** | Add the address to Suppression **immediately**. Cancel everything for them. No reply unless Charles asks. Status `lost`. Alert Charles. |
| **Out of office** | Push any scheduled follow-up to the working day after their return date. If they name an alternative contact, add them as `queued` with a note. |
| **Bounce** (mailer-daemon, "address not found") | Mark the lead `lost` with note `bounced`. Add the address to Suppression (reason: bounce). If 2 or more bounces happen in a day, set `paused = yes` and alert Charles. |
| **Anything sensitive** (complaint, legal, invoice, existing project) | Don't draft. Alert Charles with a two-line summary. |

- Every drafted reply is created in the same thread with `replyToMessageId` and labelled `MORE Agent/To review`. Any link in it follows `config/proof.md` → *How links go into a draft* (htmlBody only, read the draft back, no `google.com/url`).
- Update Leads and Log for every action.

## 3. Incoming requests (knowmore@ and the website form)

- Search for new messages delivered to knowmore@wedomore.com (`deliveredto:knowmore@wedomore.com`), and website form notifications, in the window.
- Ignore spam, vendors pitching MORE, job applications, invoices and payment threads, and anything a colleague has already answered (check the thread).
- For each real enquiry:
  1. **Classify:**
     - **studio booking:** which room and what dates;
     - **brief:** audio, video, branded content or talent;
     - **quote request;**
     - **other.**
  2. **For studio bookings, check availability** on the room calendars in `config/sources.md` for the dates they asked (use `suggest_time` or the room's events), and note what's free.
  3. **Draft a reply for Charles,** in his voice:
     - Thank them.
     - Confirm what you understood.
     - Give availability for studio requests.
     - Ask the one or two questions needed to quote.
     - **No prices.** Suggest who should be looped in (audio enquiries usually go to Joanne, production to Dalia) as a note in the alert, not in the draft.
  4. Add a row to Inbound; label the draft `MORE Agent/To review`; **alert Charles.**

## 4. Charles's instructions

- Read new replies from Charles in threads whose subject starts with `MORE Agent ·` (his replies to your summary emails). Apply instructions you understand:
  - `3B`: rewrite draft 3 with option B; replace the Gmail draft and update the sheet.
  - `skip 4`: delete draft 4 and set its lead to `skipped` (Skip reason `Charles`).
  - `pause P6` / `resume P6`: update active_plays.
  - `boost P5 +3`: update boosts.
  - `pause all` / `resume`: set paused.
  - `site live`: set site_live = yes.
- Free-text feedback ("too formal", "don't mention Netflix to agencies") goes into the Log as `feedback:` and is quoted in the next weekly report. Apply it to new drafts from then on.
- Confirm what you changed in one short reply in that thread.

## 5. Follow-ups (the 10:00 run only)

For each Sequences row with Status `scheduled` and Due date ≤ today, only Mon–Thu:
1. Re-read the full thread. If anyone other than Charles has written since email 1, cancel it (the reply step should have caught it).
2. Check the contact against Suppression.
3. Send the stored body as a reply in the same thread, from Charles. Light date updates are fine; anything else, don't change it.
4. Status `sent`, Sent at. If step 2 was sent, schedule step 3 for 7–10 working days later. Log it.

Stop sending for the day if anything looks wrong (repeated bounces, an error, `paused`).

## 6. Hot alerts

- For positive replies, meeting requests, referrals, inbound enquiries, opt-outs with complaints and escalations, send Charles one short alert email per item.
- **Subject:** `MORE Agent · reply from [Name], [Company]`
- **Body:** what they said (one line), what you drafted, the link.
- Label it `MORE Agent/Summaries`.

## 7. Finish

Set `last_inbox_check` to now. Log a one-line run summary (counts per action).
