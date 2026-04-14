---
title: "Asana Project Setup from Scratch"
task: productivity
domain: [business, nonprofit, events]
complexity: intermediate
tags: [asana, project-management, setup, tasks, workflow, organization]
claude_model: sonnet
last_tested: 2026-04-13
---

# Asana Project Setup from Scratch

## Purpose
Design and build out an Asana project with sections, tasks, subtasks, dependencies, and due dates from a brain dump or brief.

## The Prompt

```
Create an Asana project structure for {{PROJECT_NAME}}.

Goal: {{GOAL}}
Timeline: {{TIMELINE}}
Team members: {{TEAM}}
Key milestones: {{MILESTONES}}

Design the project with:
1. **Sections** — logical phases or workstreams (4-6 sections max)
2. **Tasks** — actionable items under each section (5-8 per section max, specific enough that someone knows exactly what "done" looks like)
3. **Subtasks** — only where a task genuinely has multiple steps that need tracking
4. **Assignees** — who owns each task based on the team roles
5. **Due dates** — realistic dates working backward from the final deadline, with buffer built in
6. **Dependencies** — which tasks block other tasks
7. **Milestones** — the key checkpoints that the project revolves around

Rules:
- Every task should start with a verb (Draft, Review, Send, Build, Confirm, etc.)
- No task should take more than a week — if it does, break it into subtasks
- Include a "Pre-launch checklist" or "Final review" section at the end
- Add 1-2 "buffer" tasks for things that always come up but aren't predictable

Format as a list I can build in Asana, or create it directly if you have Asana access.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{PROJECT_NAME}}` | Project name | "NECC 2026 Event Production" |
| `{{GOAL}}` | What success looks like | "Execute a 200-person, 3-day academic competition at The Mayflower Hotel with zero critical logistic failures" |
| `{{TIMELINE}}` | Start to finish | "January 15 – April 19, 2026" |
| `{{TEAM}}` | Who's involved | "Alessandra (Operations), Celeste (Event Lead), Bo (AV/Tech), Kristen (Registration), 4 student volunteers (assigned closer to event)" |
| `{{MILESTONES}}` | Key dates | "Registration opens Feb 1, Submissions close March 1, Judging complete March 20, Event April 16-19" |

## Usage Notes
- Claude can create this directly in Asana if you have the integration connected
- "Every task starts with a verb" prevents vague tasks like "Hotel stuff"
- "No task over a week" is the key constraint for realistic project tracking

## Tips
- After setup, ask: "What's the critical path? Which tasks, if delayed, push the whole project?"
- Chain with: "Create a weekly status update template I can fill in from this project"
- For recurring events: "Clone last year's project and adjust dates and lessons learned"
- Ask: "Add a 'Lessons Learned' section with placeholder tasks for post-event capture"
