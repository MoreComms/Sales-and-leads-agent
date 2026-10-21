# MORE · Sales & Leads Agent

An automated pipeline that finds the right people for MORE's services, researches them, writes outreach in Charles's voice, follows up, reads the replies and books meetings for him to take forward.

**Status: set up, first drafts in review (21 Oct 2026).** The agent runs as scheduled Claude sessions on Charles's existing Claude plan, through his Google Workspace. This repo holds its instructions (`CLAUDE.md`, `agent/jobs/`) and settings (`config/`). Its memory is the *MORE Sales Agent* sheet in Charles's Drive. The plan behind it is in `docs/`.

## The idea in six lines

1. **Warm first, then signals, never generic lists.** Start with 15 years of past clients and dormant contacts, reconnecting on something genuinely relevant to them. Then go after accounts where something just happened that creates a need: an agency won an account, a brand is planning Ramadan, an RFQ dropped, a production is coming to the UAE.
2. **Organised by service, balanced, not ranked.** Eleven *plays* map MORE's six capabilities to the website's five doors (brands, agencies, studios, creators, investors). Each week the new-contact slots are shared evenly across them.
3. **Charles is the case study.** Every email goes from his own wedomore.com mailbox, in his voice, with his signature. No extra domains. He approves every first touch from his phone. Daniel, Jojo and Elsa join later if it works.
4. **Few, hand-picked, high-potential leads.** At most 40 new people a week, plus reactivations. Only people with a strong fit and a fresh reason; everyone else is watched, not emailed.
5. **From reply to meeting, handled.** Replies are classified within the hour, times proposed from Charles's calendar, and a prep brief lands on the morning of the call. Everything is tracked in the agent's own Google Sheet.
6. **Safe by design.** Strict caps and an automatic pause protect wedomore.com. Opt-outs are global and permanent. No cold WhatsApp, no LinkedIn bots, no invented facts, nothing named beyond the website without Charles's tap.

## Read the plan

| Doc | What's in it |
|---|---|
| [01 · What MORE sells, and to whom](docs/01-what-more-sells.md) | The six capabilities, the five doors, the eleven plays, the balanced weekly slate, proof and price rules |
| [02 · Lead sourcing](docs/02-lead-sourcing.md) | Warm data, the signal playbook, finding contacts, scoring and tiers, 2026 market context |
| [03 · Outreach playbook](docs/03-outreach-playbook.md) | Message rules, channels, timing, sequences, value-first hooks, example messages, reply handling, meetings |
| [04 · Architecture](docs/04-architecture.md) | Pipeline, components, the Claude layer, data model, integrations, stack, repo layout |
| [05 · Guardrails and compliance](docs/05-guardrails-and-compliance.md) | Hard rules, autonomy levels, deliverability from wedomore.com, compliance, AI safeguards |
| [06 · Roadmap, metrics and costs](docs/06-roadmap-metrics-costs.md) | Phases to Ramadan 2027 and beyond, targets, monthly running costs, risks |
| [07 · Decisions](docs/07-decisions.md) | What's agreed, and **what's still needed before building** |
| [08 · Ramadan 2027 target brands](docs/08-ramadan-target-brands.md) | 43 approved brands for Ramadan branded entertainment and content (no sponsorship pitching) |

## How it runs (Dubai time, Monday to Friday)

| Time | Job |
|---|---|
| 07:15 | Signals scan: news, tenders, podcasts → the sheet |
| 07:45 | Morning slate: ~8 new drafts across plays + reactivations in Charles's Gmail, and a summary email |
| Hourly, 09:00–18:00 | Inbox check: replies, incoming requests, meeting times, Charles's instructions; follow-ups at 10:00 |
| 17:45 | Evening wrap email |
| Friday 11:45 | Weekly report |

**Cost: $0 extra.** **Charles sends every first email himself.**

## Repository

```
CLAUDE.md        operating manual every run reads first
agent/jobs/      one file per scheduled job
config/          plays, guardrails, proof, voice, sources, sheet layout
docs/            the plan (01–08)
```
