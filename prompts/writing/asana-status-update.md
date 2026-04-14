---
title: "Asana Status Update Generator"
task: writing
domain: [business, nonprofit, events]
complexity: beginner
tags: [asana, status-update, reporting, project-management, progress]
claude_model: sonnet
last_tested: 2026-04-13
---

# Asana Status Update Generator

## Purpose
Generate a project status update from Asana task data — for board reports, team check-ins, or stakeholder updates.

## The Prompt

```
Write a status update for the {{PROJECT_NAME}} project.

Here's where things stand:
{{TASK_STATUS}}

Format as a project status update with:
- **Status** (On Track 🟢 / At Risk 🟡 / Off Track 🔴) — be honest
- **Summary** — 2 sentences on overall progress
- **Completed this week** — what got done
- **In progress** — what's actively being worked on
- **Blocked / At Risk** — anything stuck and why
- **Coming up next week** — what's ahead
- **Asks** — anything I need from the reader (decisions, approvals, resources)

Audience: {{AUDIENCE}}
Tone: {{TONE}}
Length: Under {{LENGTH}} words.

Don't sugarcoat. If we're behind, say so and say what we're doing about it.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{PROJECT_NAME}}` | Project | "NECC 2026 Production" |
| `{{TASK_STATUS}}` | Current state | Paste from Asana or describe: "Registration: 185/200 target. Hotel EOs: 6 of 8 finalized, 2 pending AV confirmation. Judging setup in Award Force: complete. Printed materials: badges ordered, programs still in design. Budget: $2K under, but AV quote came in $800 over estimate." |
| `{{AUDIENCE}}` | Who reads it | "Event committee (Celeste, Bo, Kristen)" |
| `{{TONE}}` | How formal | "Casual team update — we're all in the trenches together" |
| `{{LENGTH}}` | Max words | "200" |

## Usage Notes
- Paste your Asana task list or search results directly — Claude extracts the status
- "Don't sugarcoat" is critical — most AI status updates default to optimistic
- If Claude has Asana access, ask it to pull the data directly

## Tips
- Run weekly at the same time to build a rhythm
- Chain with: "Post this as a status update on the Asana project"
- For board reporting: "Elevate this into a formal board report paragraph — more polished, less tactical"
- Ask: "Based on this status, what should I be worried about that I'm not mentioning?"
