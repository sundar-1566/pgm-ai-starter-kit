---
name: meeting-to-jira
description: Turn a meeting transcript or notes into decisions, risks, and action items, then draft Jira tickets for the PgM to confirm, edit, or drop before anything is created. Use after a project sync, steering committee, QBR, or leadership session.
---

# Meeting → Decisions, Risks, and Draft Jira Tickets

**Who it's for:** a PgM who leaves every meeting with a page of notes and 30 minutes of cleanup.
**What it gives back:** a clean decision and action log plus ready-to-create tickets. The PgM stays in control of what goes into Jira.

## Inputs
- A meeting transcript (Zoom, Meet, or Teams) or typed notes
- Attendee list with roles (helps assign owners)
- The project's Jira project key and its usual issue types
- Optional: the open risk log, so the skill can update existing risks instead of duplicating them

## Steps
1. **Read the whole transcript.** Separate what was **decided** from what was only **discussed**. If something sounds decided but nobody confirmed it, mark it "Needs confirmation."
2. **Pull out four lists:**
   - **Decisions:** what was decided, by whom, and any condition attached
   - **Actions:** task, owner (a named person, never "the team"), and due date (use the date if stated; if not, write "No date set")
   - **Risks and issues:** what could go wrong, likely impact, and owner. Match each to an existing risk if there is one.
   - **Open questions:** things nobody answered
3. **Draft Jira tickets** for each action:
   - Summary (verb first, under 80 characters)
   - Description: context from the meeting with a quote or timestamp, the acceptance criteria, and a link to the notes
   - Assignee, due date, labels (`from-meeting`, plus the meeting name), and a link to the parent epic if known
4. **Show the drafts in a confirmation table.** For each ticket the PgM chooses **Create / Edit / Drop**.
5. **Create only what the PgM approves.** Then post the meeting summary to the project channel as a **draft** for the PgM to send.

## Output template
```
MEETING: <name>, <date>    Attendees: <names>
Decisions (n)
1. <decision>, decided by <name>. Condition: <if any>
Actions → Draft Jira tickets (n)
| # | Summary | Owner | Due | Epic | Confirm? |
Risks / issues (n)
| Risk | Impact | Owner | New or existing |
Open questions
Needs confirmation (sounded decided, wasn't confirmed)
```

## Guardrails
- **Nothing is created in Jira without the PgM confirming each ticket.**
- Never assign a ticket to someone who wasn't in the meeting or named in it.
- Quote the transcript for every decision, so anyone can check it.
- Drop side conversations and personal remarks from the summary.

## How to tell it's working
- Minutes from meeting end to actions logged (target: under 10)
- Share of drafted tickets created without edits
- Actions with a named owner and a due date (target: 100%)
