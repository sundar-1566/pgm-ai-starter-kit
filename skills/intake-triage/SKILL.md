---
name: intake-triage
description: Turn a raw portfolio request (Slack message, email, or form) into a complete intake record, check it for overlap with active projects, and draft a first-pass priority score with reasons for the PgM and portfolio council to review. Use when new GTM/CX work requests arrive.
---

# Intake Triage

**Who it's for:** the PgM running intake for a portfolio of 50+ projects a quarter, where requests arrive half-filled and some duplicate work already under way.
**What it gives back:** every request arrives at the prioritization meeting complete, de-duplicated, and pre-scored.

## Inputs
- The raw request: Slack message, email, or intake form
- The active portfolio list: name, goal, owner, teams involved, systems touched, dates
- Your scoring rubric. If you don't have one, use the default below.
- This quarter's company or GTM priorities

## Steps
1. **Structure the request** into the intake fields:
   problem, who is affected, business goal, requesting leader, teams needed, systems touched, deadline (and why), and how success is measured.
2. **List what's missing** and draft the follow-up questions to the requester, worded so they're quick to answer.
3. **Check for overlap** with active projects: same goal, same systems, same teams, or clashing dates. For each match, name the project and explain in one line why it looks similar.
4. **Draft a score** using the rubric and show the reasoning for each factor:
   | Factor | Weight | What it means |
   |---|---|---|
   | Revenue or retention impact | 30% | Pipeline, bookings, renewal, expansion |
   | Field productivity | 25% | Seller, SE, or CSM hours saved |
   | Customer impact | 20% | Faster time to value, fewer escalations |
   | Risk reduction or compliance | 15% | Audit, security, revenue accounting |
   | Effort, inverse | 10% | Smaller effort scores higher |
5. **Recommend a path:** fast-track, regular queue, merge with project X, or decline with a reason. Mark it clearly as **a draft for the portfolio council**.

## Output template
```
INTAKE: <title>   Requested by: <name>   Received: <date>
Structured request (fields above)
Missing info → questions for requester
Possible overlap: <project>, <why similar>
Draft score: <n>/100   Reasoning per factor
Recommended path (DRAFT): <path>, <one-line reason>
```

## Guardrails
- The score is a **starting point for discussion**. People make the priority call.
- Don't judge the requester. Score the request.
- Read-only on the portfolio list.

## How to tell it's working
- Requests complete on first review (target: 90%+)
- Duplicates caught before kickoff
- Days from request to decision
