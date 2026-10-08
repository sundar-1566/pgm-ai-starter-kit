---
name: uat-from-qa-pass
description: When a Jira story moves to "QA Passed," read the story, its acceptance criteria, and linked docs; draft business-user UAT scripts; check that every acceptance criterion is covered; and create draft UAT tasks for the business owner to approve. Use for GTM/CX system changes (CRM, quoting, billing, support tools) that need business sign-off.
---

# QA Pass → UAT Scripts (event-triggered agent)

**Who it's for:** PgMs delivering GTM/CX system changes, where business testers wait days for someone to write UAT scripts after QA finishes.
**What it gives back:** UAT starts the same day QA passes, and every acceptance criterion is covered.

## Trigger
A Jira issue changes status to **QA Passed** (or your team's equivalent). The trigger can be a Jira automation rule, a webhook, or a PgM typing "run UAT for <key>."

## Inputs
- The Jira story: summary, description, **acceptance criteria**, components, fix version
- Linked items: the requirements doc, design notes, QA test cases and their results
- Business owner and tester list for the affected team (Sales Ops, Deal Desk, CS Ops, Support Ops)
- The UAT script template, if your team already has one (otherwise use the one below)

## Steps
1. **Read the story and acceptance criteria.** If the acceptance criteria are missing or vague, **stop**. Comment on the story asking for clear criteria and tag the PgM. Don't guess.
2. **Write scripts in business language**, one or more per acceptance criterion:
   - Who is testing (role), the starting conditions, and the test data to use
   - Numbered steps written in screen terms ("Open the Opportunity, click Add Product")
   - The expected result for each step
   - At least one **negative test** per criterion (what should be blocked or rejected)
3. **Check coverage.** Build a table mapping each acceptance criterion to the scripts that test it. Flag any criterion with no script.
4. **Reuse QA's work.** Point to the QA test cases already passed so business testers don't repeat technical checks.
5. **Create draft UAT sub-tasks** under the story, one per tester role, assigned to the named business tester, with the script attached. Leave them in **Draft / To Do**.
6. **Stop for approval.** The business owner or PgM approves the scripts. Only then notify the testers.

## Script template
```
UAT-<story key>-<n>: <what's being tested>
Tester role: <e.g., Deal Desk analyst>   Acceptance criterion: AC-<n>
Starting conditions: <account / user / data needed>
Steps                                   | Expected result
1. ...                                  | ...
Negative test: <action that should be blocked> → <expected block/message>
Pass / Fail / Notes: ______
```

## Guardrails
- **Draft only.** The agent can create sub-tasks and comments. It **cannot** change the story's status, close tickets, or touch production systems.
- Use only test or sandbox accounts in scripts. Never use real customer names or data.
- Log every Jira action the agent takes on the story as a comment ("UAT agent created 3 draft sub-tasks").

## How to tell it's working
- Days from QA pass to UAT start (target: same day)
- Share of acceptance criteria covered by a script (target: 100%)
- Defects found in UAT versus after release (more found in UAT is good)
