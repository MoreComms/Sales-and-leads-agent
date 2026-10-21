# Job: signals scan (Mon–Fri, 07:15 Dubai)

**Goal:** fill the Signals tab with real, recent reasons to contact specific companies, so the morning slate has good material. Also catch tenders and RFQs for Charles.

Read first: `CLAUDE.md`, `config/plays.md`, `config/sources.md`, `config/sheet.md`.

## 0. Should I run?

Stop if Settings `paused = yes`, or if it's Saturday or Sunday.

## 1. Web signals for P1–P8

- For each active play, run 2–4 searches from `config/sources.md` focused on the last 14 days, UAE first (Kuwait and Qatar for P1).
- Keep a result only if:
  - it names a specific company, and ideally a person;
  - something happened that creates a need MORE can meet;
  - you can see the date and the URL.
- Skip anything already in the Signals tab: same company and same event.
- Add rows: Date, Play, Company, What happened (one line), URL, Strength (1–5: 5 = clear, recent, high-value need).
- Aim for quality, about 3–8 good signals a day across all plays. Zero is fine on a quiet day.

## 2. Tenders and RFQs (P9)

- Search Charles's Gmail for new tender alerts since yesterday: the senders in `config/sources.md`, or `newer_than:1d (tender OR RFQ OR RFP OR "request for proposal" OR "invitation to bid")`.
- Also search news for RFQs from DET, DCT, Modon, Emaar or Dubai Holding.
- For each relevant one (content, video, podcasts, audio, events, social, branded content, studio services), send Charles an alert email:
  - **Subject:** `MORE Agent · RFQ: [title], due [date]`
  - **Body:**
    - who is buying, what, the deadline and the link;
    - fit from 1 to 5 and why;
    - a two-line bid or no-bid take (team capacity, margin risk, whether MORE has done similar).
- Add it to Signals with Play `P9`.
- Never register, apply or reply on a portal.

## 3. Finish

Log the counts (signals added per play, RFQs found).
