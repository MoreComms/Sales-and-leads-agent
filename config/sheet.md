# The "MORE Sales Agent" sheet

The agent's memory. It lives in Charles's Drive, in the folder **MORE Sales Agent**.

- **spreadsheetId:** `1_eKZFfb052J5t8Kn1H99WBtl6plXAp3VoKkYebVHiKg`
- **Row 1 of every tab is the header row.** Never reorder columns; add new columns only at the right.
- **Dates:** ISO `YYYY-MM-DD`. Times: `YYYY-MM-DD HH:MM` in Dubai time.

## Leads

One row per person the agent considers.

| Column | Meaning |
|---|---|
| Lead ID | `L-YYYYMMDD-NN` |
| Added | Date added |
| Play | P0–P8 |
| Tier | A, B or C |
| Company | |
| Contact | Full name |
| Title | |
| Email | Work address only |
| Country | |
| Signal | What happened, one line |
| Source URL | Where the signal came from |
| Fit / Timing / Value | 0–5 each |
| Research | 3–6 facts, each followed by its source URL |
| Status | `queued` · `linkedin-it` · `drafted` · `sent` · `replied-positive` · `replied-neutral` · `replied-negative` · `meeting` · `won` · `lost` · `nurture` · `skipped` |
| Skip reason | collision · suppressed · personal address · KSA · weak fit · other |
| Draft ID | Gmail draft id for email 1 |
| Thread ID | Gmail thread id once sent |
| Options offered | Personalisation options shown to Charles, e.g. `3A: FoodTok / 3B: Samsung via Craft` |
| Next step | |
| Next date | |
| Notes | |

## Sequences

The follow-ups, written when the lead is drafted.

| Column | Meaning |
|---|---|
| Lead ID | |
| Thread ID | Filled when Charles sends email 1 |
| Step | 2 or 3 |
| Due date | Set when email 1 is sent |
| Body | The follow-up text |
| Status | `waiting-for-email-1` · `scheduled` · `sent` · `cancelled` |
| Sent at | |

## Signals

| Column | Meaning |
|---|---|
| Date | |
| Play | |
| Company | |
| What happened | |
| URL | |
| Strength | 1–5 |
| Used by | Lead ID, if used |

## Inbound

Incoming requests through knowmore@ or the website form.

| Column | Meaning |
|---|---|
| Received | |
| From | |
| Company | |
| Type | `studio booking` · `brief` · `quote` · `other` |
| Details | Rooms, dates, what they're making |
| Availability | What the room calendars showed |
| Draft ID | |
| Status | `drafted` · `answered` · `forwarded` |

## Suppression

Never contacted again. The agent only ever adds rows here.

| Column | Meaning |
|---|---|
| Email or domain | |
| Reason | |
| Date | |
| Source | Reply, Charles, bounce |

## Log

| Column | Meaning |
|---|---|
| Time | |
| Job | |
| Action | |
| Lead ID | |
| Detail | |

## Settings

| Key | Default | Meaning |
|---|---|---|
| `paused` | `no` | `yes` stops all drafting and sending: the kill switch |
| `weekly_new_cap` | `40` | New first-touch drafts per week |
| `daily_new_cap` | `10` | New first-touch drafts per day |
| `daily_reactivation_cap` | `5` | P0 drafts per day |
| `active_plays` | `P0,P1,P2,P3,P4,P5,P6,P7,P8,P9,P10` | Plays the slate may use |
| `boosts` | *(empty)* | e.g. `P5:+5` adds 5 weekly slots to P5 |
| `site_live` | `no` | `yes` once the new website is published; unlocks deep page links. The launch itself is never used as a reason to reach out. |
| `auto_scheduling` | `off` | `on` lets the agent confirm meeting times itself |
| `personal_contacts` | *(empty)* | Emails Charles never wants the agent to touch |
| `last_inbox_check` | | Set by the inbox check |

---

**Setup record:** sheet created 2026-10-21 → spreadsheetId `1_eKZFfb052J5t8Kn1H99WBtl6plXAp3VoKkYebVHiKg`, folder `1_z_QhwZz9wOJZP0IqJ_JXFwxfL5zdMm_`.
