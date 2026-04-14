---
title: "Asana Workload Review & Rebalancing"
task: analysis
domain: [business, nonprofit, general]
complexity: intermediate
tags: [asana, workload, capacity, delegation, team-management, burnout]
claude_model: sonnet
last_tested: 2026-04-13
---

# Asana Workload Review & Rebalancing

## Purpose
Audit task assignments across a team to find overload, underutilization, and rebalancing opportunities.

## The Prompt

```
Review the current workload distribution for {{PROJECT_OR_TEAM}}.

Here's everyone's task list for the next {{TIMEFRAME}}:
{{TASK_ASSIGNMENTS}}

Analyze:
1. **Load per person** — count tasks, estimate hours, flag anyone with more than {{MAX_HOURS}} hours of work in the timeframe
2. **Overloaded** — who has too much? Which of their tasks could be reassigned?
3. **Underutilized** — who has capacity? What could they take on?
4. **Bottleneck people** — who is a dependency for the most tasks? (If they get sick, what breaks?)
5. **Due date clustering** — are too many things due the same day? Suggest spreading them out.
6. **Rebalancing recommendation** — specific reassignments with rationale

Be practical — don't reassign tasks to people who don't have the skills for them. Flag if you need more context about someone's capabilities.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{PROJECT_OR_TEAM}}` | What you're reviewing | "NECC 2026 event team" |
| `{{TIMEFRAME}}` | Period to review | "next 2 weeks (April 1-14)" |
| `{{TASK_ASSIGNMENTS}}` | Everyone's tasks | Paste from Asana: "Alessandra: 14 tasks. Celeste: 8 tasks. Bo: 5 tasks. Kristen: 11 tasks. Volunteers: 2 tasks." Or upload the Asana export. |
| `{{MAX_HOURS}}` | Overload threshold | "40 hours" |

## Usage Notes
- If Claude has Asana access, ask it to pull task lists directly instead of pasting
- Honest hour estimates matter more than task counts — one complex task can equal five simple ones
- Run this weekly during crunch time

## Tips
- Follow up with: "Draft a Slack message to [person] asking them to take on [reassigned tasks] — make it a request, not a dump"
- Ask: "If I had to cut my own task list by 30%, what should go?"
- Chain with the weekly priority planning prompt for your personal list
- For recurring overload: "This person is overloaded every cycle — what's the systemic fix?"
