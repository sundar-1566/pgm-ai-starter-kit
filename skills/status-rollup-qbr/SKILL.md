---
name: status-rollup-qbr
description: Pull weekly project updates from Slack, email, meeting notes, and Jira; match them to each project; set Red/Amber/Green with reasons; draft the portfolio roll-up for PgM review. At quarter end, turn the same data into a QBR pre-read. Use when someone asks for a weekly status, portfolio roll-up, exec update, or QBR pre-read.
---

# Status Roll-up → QBR Pre-read

**Who it's for:** a program manager running 10–100 projects who rebuilds status by hand every week.
**What it gives back:** a draft roll-up in minutes. The PgM spends their time on judgment, not copy-paste.

## Inputs (use whatever is available; say what was missing)
- **Jira:** issues updated in the last 7 days for the portfolio's projects (status, due date, blockers, assignee changes)
- **Slack:** messages in each project channel from the last 7 days
- **Email:** threads tagged or labeled with a project name
- **Meeting notes:** Google Docs or transcripts from this week's project meetings
- **Last week's roll-up** (so changes can be called out)
- **Portfolio list:** project name, owner, executive sponsor, target date, tier

If no connectors are set up, the PgM can paste exports or text. The skill works the same way.

## Steps
1. **Collect.** Gather each source for the past 7 days. List the sources actually read at the top of the draft.
2. **Match each update to a project.** Use the project name, Jira key, channel name, or owner. If an update doesn't clearly match, put it in an "Unmatched" list. Never guess.
3. **Pull out the facts** for each project: progress since last week, next milestone and date, blockers, decisions needed, and asks of leadership.
4. **Set Red / Amber / Green** using the rules below. Always give the reason in one line, with the source.
   - **Green:** on track for the next milestone and no open blocker older than 5 days
   - **Amber:** milestone at risk (date slipped or blocker open 5+ days) and a recovery plan exists
   - **Red:** milestone missed or will be missed, no recovery plan, or an executive decision is needed
5. **Flag changes:** any project whose color changed since last week, and any project with **no update at all** (silence is a risk signal).
6. **Draft the roll-up** using the template below. Lead with what leaders need to decide.
7. **Stop for PgM review.** Present the draft. Do not post, send, or publish anything until the PgM approves.

## Output template: weekly roll-up
```
PORTFOLIO STATUS: week of <date>    Sources read: Jira, Slack (#..), Email, Notes (n docs)
Headline: <one sentence: what leaders need to know>

Decisions needed this week
- <project>: <decision> (owner, by when)

Changed color since last week
- <project>: Amber → Red. <reason> [source]

Red / Amber
| Project | Color | Why (1 line) | Next milestone | Owner | Ask |

Green (one line each)
No update received (follow up): <projects>
Unmatched updates (PgM to place): <items>
```

## Quarter end: QBR pre-read
Use the last 13 weekly roll-ups:
1. **Portfolio health:** count of projects by color, and how the mix moved over the quarter
2. **Delivered:** projects closed, each with the business result in one line (revenue, field time saved, customer impact)
3. **Slipped:** each slip with its root cause grouped into types (capacity, dependency, scope, decision delay)
4. **Top 3 risks for next quarter**, each with a proposed mitigation and an owner
5. **Asks of the exec team:** decisions, trade-offs, and resourcing
Keep it to 2 pages. Write in plain business language and drop any project jargon.

## Guardrails
- Read-only on every source. Drafts only, so nothing is sent or posted without PgM approval.
- Every color and every claim cites its source. If the evidence is thin, say "unconfirmed."
- Never include confidential HR or compensation details in a roll-up.

## How to tell it's working
- PgM minutes per weekly roll-up (target: down 60%+)
- Rewrite rate: the share of the draft the PgM changes (target: under 20% by week 4)
- Roll-ups sent on time
