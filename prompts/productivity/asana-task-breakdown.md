---
title: "Asana Task Breakdown & Delegation"
task: productivity
domain: [business, nonprofit, general]
complexity: beginner
tags: [asana, tasks, delegation, breakdown, subtasks, assignment]
claude_model: sonnet
last_tested: 2026-04-13
---

# Asana Task Breakdown & Delegation

## Purpose
Take a big, vague task and break it into Asana-ready subtasks with clear owners and deadlines.

## The Prompt

```
I have this task in Asana that's too big and vague:
"{{BIG_TASK}}"

Context: {{CONTEXT}}
Deadline: {{DEADLINE}}
People available: {{PEOPLE}}

Break this into subtasks that are:
- Specific enough that the assignee doesn't need to ask "what does this mean?"
- Each completable in 1-3 days
- Each starting with an action verb
- Assigned to the right person based on their role
- Sequenced with realistic dates working backward from the deadline

Also tell me:
- Which subtask is the bottleneck (if this one slips, everything slips)?
- What can run in parallel?
- Is anyone overloaded? If so, what should I redistribute?

Format as an Asana-ready list:
☐ Task name | Assignee | Due date | Depends on
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{BIG_TASK}}` | The vague task | "Prepare all event materials for NECC" |
| `{{CONTEXT}}` | What it involves | "Printed programs, name badges, signage, table tents, judge packets, volunteer packets, awards certificates" |
| `{{DEADLINE}}` | When it's due | "April 14 (2 days before event)" |
| `{{PEOPLE}}` | Who's available | "Me (design + coordination), Kristen (registration data for badges), Bo (AV specs for signage), student volunteer team (assembly)" |

## Usage Notes
- This is the single most-used prompt for project management
- The "Asana-ready list" format means you can literally copy each line into Asana
- Sonnet handles task breakdowns quickly and well

## Example Output
> ☐ Export final attendee list from Cvent | Kristen | April 7 | —
> ☐ Design name badge template | Alessandra | April 8 | —
> ☐ Merge attendee data into badge template | Alessandra | April 9 | Depends on: Export list, Design template
> ☐ Send badge file to printer | Alessandra | April 10 | Depends on: Merge data
> ☐ **BOTTLENECK** Pick up printed badges | Volunteer TBD | April 13 | Depends on: Send to printer
>
> **Parallel track:** Signage design can run simultaneously with badge production.
> **Overload flag:** Alessandra has 4 tasks due April 8-10. Consider delegating badge template to a design contractor.

## Tips
- Run this whenever you catch yourself writing a task that's actually a project
- Chain with: "Now add these to my Asana project under the [section name] section"
- For recurring tasks: "Which of these should be templated for next year?"
