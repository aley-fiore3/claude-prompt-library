---
title: "Day-of-Event Run Sheet Generator"
task: events
domain: [events, logistics]
complexity: advanced
tags: [run-sheet, timeline, event-management, logistics, day-of, coordination]
claude_model: opus
last_tested: 2026-04-13
---

# Day-of-Event Run Sheet Generator

## Purpose
Create a minute-by-minute run sheet for event day, with who does what and when.

## The Prompt

```
Create a day-of run sheet for {{EVENT_NAME}} on {{DATE}}.

Schedule:
{{SCHEDULE}}

Staff/roles:
{{STAFF}}

Venue details:
{{VENUE}}

For each time block, include:
- Exact time (to the minute for transitions)
- What's happening (attendee-facing)
- What's happening behind the scenes (staff-facing)
- Who is responsible
- Setup/AV/catering notes for that block
- Contingency if something runs late

Add 15-minute buffer warnings before every transition. Flag any time where two things need to happen simultaneously.

Format as a table I can print and carry on a clipboard.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{EVENT_NAME}}` | Event name | "NECC Day 2 — Competition Rounds" |
| `{{DATE}}` | Specific date | "April 17, 2026" |
| `{{SCHEDULE}}` | The timeline | "8:00 breakfast, 9:00 Round 1 presentations (3 rooms), 12:00 lunch, 1:00 Round 2, 4:00 break, 6:00 Judges Dinner" |
| `{{STAFF}}` | Your team | "Celeste (Event Lead), Bo (AV/Tech), Kristen (Registration), Me (Operations), 4 student volunteers" |
| `{{VENUE}}` | Where | "Mayflower Hotel — Grand Ballroom, State Room, Cabinet Room, Foyer" |

## Usage Notes
- Opus handles the complexity of simultaneous events better
- "Format as a table I can print" ensures readability on paper
- The "contingency if late" section is worth gold on event day

## Tips
- Create one run sheet per day for multi-day events
- Follow up with: "Now create a simplified version for volunteers — just their tasks, no staff info"
- Add: "What are the 3 most likely things to go wrong and how do we handle each?"
- Print two copies — one for you, one for your backup
