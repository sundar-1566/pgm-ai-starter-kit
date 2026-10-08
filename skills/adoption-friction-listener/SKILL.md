---
name: adoption-friction-listener
description: Read field feedback (Slack channels, support or ops tickets, survey comments, enablement Q&A) about a newly rolled-out GTM/CX process or tool, group it into friction themes, estimate how widespread each is, spot workarounds, and draft fixes and a "you said, we did" note. Use 1–8 weeks after any process or tool rollout, including AI tool rollouts.
---

# Adoption Friction Listener

**Who it's for:** the PgM or change lead who rolled out a new process or tool and needs to know, honestly, why people are or aren't using it.
**What it gives back:** a weekly list of the top friction points with evidence, so fixes target the real problem instead of the loudest complaint.

## Inputs
- **Feedback sources** for the rollout period: field Slack channels, ops and support tickets tagged to the process, survey free-text, office-hours Q&A, enablement session chat
- **Adoption numbers**, if available: usage counts, completion rates, the share of records done the new way versus the old way
- **What changed:** the rollout note or training deck, so the skill knows what "correct use" looks like

## Steps
1. **Collect** feedback since the rollout or the last run. Remove names. Keep the role and region only.
2. **Group into themes.** Each piece of feedback gets one primary theme:
   - **Don't know how** (training or documentation gap)
   - **Takes too long** (too many steps or fields, slow tool)
   - **Doesn't fit my case** (the process breaks for some deal types, regions, or segments)
   - **Don't see why** (value not explained, or a manager not reinforcing it)
   - **Broken** (a bug, access problem, or data problem)
   - **Don't trust it** (output quality, accuracy, or security worries, which is common for AI tools)
3. **Size each theme:** number of mentions, number of distinct teams or regions, and the trend versus last run.
4. **Spot workarounds:** spreadsheets, side channels, "I just email Deal Desk." A workaround is the strongest friction signal and usually the most fixable.
5. **Draft fixes** for the top 3 themes, each with an owner type (enablement, ops, IT, or the process owner) and effort (small, medium, or large).
6. **Draft a "you said, we did" note** for the field covering the fixes already made. This builds trust and drives the next wave of adoption.
7. **Stop for review** by the process owner before anything is shared.

## Output template
```
ADOPTION PULSE: <process/tool>, week <n> since rollout
Adoption: <metric> (<trend>)       Feedback items read: <n> from <sources>
Top friction themes
| Theme | Mentions | Teams/regions | Trend | Example (no names) |
Workarounds seen: <list>
Recommended fixes (DRAFT)
| Fix | Theme | Owner | Effort |
"You said, we did" draft note
```

## Guardrails
- Remove names and personal details. Report on patterns, never on individuals.
- Quote feedback exactly. Don't make complaints sound softer or harsher.
- This is a listening tool, **not** a compliance-monitoring tool. Say so when it's introduced to the field.

## How to tell it's working
- Time from a friction point first appearing to a fix shipping
- Adoption rate trend after each "you said, we did" cycle
- Workarounds retired
