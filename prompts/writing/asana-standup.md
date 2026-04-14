---
title: "Asana Standup & Team Coordination"
task: writing
domain: [business, nonprofit, general]
complexity: beginner
tags: [asana, standup, team, coordination, daily, check-in, slack]
claude_model: sonnet
last_tested: 2026-04-13
---

# Asana Standup & Team Coordination

## Purpose
Generate a daily or weekly standup update from Asana task data, formatted for Slack, email, or a meeting.

## The Prompt

```
Generate a {{FREQUENCY}} standup for {{PROJECT_OR_TEAM}}.

My tasks:
{{MY_TASKS}}

Team tasks I need visibility on:
{{TEAM_TASKS}}

Format:
**Done:** What I completed since last standup
**Doing:** What I'm working on today/this week
**Blocked:** Anything I need help with (and from whom)
**FYI:** Anything the team should know

Keep it to {{LENGTH}} — this should take 30 seconds to read.

Channel: {{CHANNEL}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{FREQUENCY}}` | How often | "daily" or "weekly" |
| `{{PROJECT_OR_TEAM}}` | Context | "NECC event team" |
| `{{MY_TASKS}}` | Your current list | Paste from Asana or describe |
| `{{TEAM_TASKS}}` | What to flag | "Celeste's EO revisions, Bo's AV setup confirmation, Kristen's badge data export" |
| `{{LENGTH}}` | Max length | "5 lines max" |
| `{{CHANNEL}}` | Where it goes | "Slack #necc-2026" |

## Usage Notes
- If Claude has Asana + Slack access, it can pull tasks and post directly
- "30 seconds to read" prevents the standup from becoming a novel
- Works for async standups (Slack) or live meeting prep

## Example Output
> **Done:** Finalized 6 of 8 hotel EOs, submitted Award Force judge assignments
> **Doing:** Reviewing last 2 EOs (AV-dependent), designing badge template
> **Blocked:** Need AV quote from Bo by EOD to finalize Grand Ballroom EO
> **FYI:** Registration at 192/200 — likely hitting target by Friday

## Tips
- Automate this: "Set up a recurring reminder to run this prompt every Monday at 8am"
- Chain with: "Post this to Slack #necc-2026"
- For meeting prep: "Turn this into 3 talking points for my 10am check-in with Celeste"
