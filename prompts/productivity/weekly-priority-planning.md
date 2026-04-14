---
title: "Weekly Priority Planning System"
task: productivity
domain: [general, business, nonprofit]
complexity: intermediate
tags: [planning, priorities, weekly-review, time-management, GTD]
claude_model: sonnet
last_tested: 2026-04-13
---

# Weekly Priority Planning System

## Purpose
Turn a brain dump of everything on your plate into a prioritized, actionable weekly plan.

## The Prompt

```
Here's everything on my plate this week:
{{BRAIN_DUMP}}

My fixed commitments this week (meetings, deadlines, travel):
{{FIXED_COMMITMENTS}}

Help me plan my week:

1. **Sort into:** Must-do (consequences if missed), Should-do (important but flexible), Could-do (nice to have)
2. **Flag** anything that's actually someone else's responsibility that I'm holding onto
3. **Identify** the single most important thing I should do Monday morning
4. **Suggest** what to defer or delegate — I can't do all of this
5. **Map** the must-dos to specific days based on my fixed commitments

Be ruthless. If something isn't important, say so.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{BRAIN_DUMP}}` | Everything in your head | "Finalize NECC event orders, review Cvent registration, email Celeste about AV, pack for DC trip, submit expense reports, draft Italy packing list, follow up with 3 grant contacts, update lending dashboard, call Mom, vet appointment for Saverio..." |
| `{{FIXED_COMMITMENTS}}` | What's locked in | "Mon: staff meeting 10am. Tue: flight to DC at 2pm. Wed-Sat: NECC conference. Sun: recovery day." |

## Usage Notes
- The "be ruthless" instruction prevents Claude from being polite about your overcommitment
- "Flag anything that's someone else's responsibility" catches delegation opportunities
- Run this every Sunday evening or Monday morning

## Tips
- Follow up with: "Create calendar blocks for the must-dos"
- If the list is still too long after sorting, ask: "What happens if I skip each should-do? Give me real consequences."
- Save your brain dump format — it gets faster each week
