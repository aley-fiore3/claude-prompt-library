---
title: "Post-Event Survey Generator"
task: events
domain: [events, cvent]
complexity: intermediate
tags: [survey, feedback, event-management, post-event, cvent]
claude_model: sonnet
last_tested: 2026-04-13
---

# Post-Event Survey Generator

## Purpose
Create a targeted post-event survey with questions tailored to different attendee types.

## The Prompt

```
Create a post-event survey for {{EVENT_NAME}}.

Attendee types to survey (each gets a slightly different version):
{{ATTENDEE_TYPES}}

For each attendee type, create:
- 5-7 questions max (short surveys get higher response rates)
- Mix of: 1 overall satisfaction (1-10), 2-3 specific ratings (Likert scale), 1-2 open-ended
- Questions specific to THEIR experience (judges care about different things than students)

Event details for context: {{EVENT_DETAILS}}

Things I specifically want to learn: {{LEARNING_GOALS}}

Format each survey section so I can copy it directly into {{SURVEY_PLATFORM}}.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{EVENT_NAME}}` | Event name | "National Ethics Case Competition 2026" |
| `{{ATTENDEE_TYPES}}` | Different audiences | "Students/competitors, Judges, Faculty advisors, Organizers/staff" |
| `{{EVENT_DETAILS}}` | Key facts | "3-day academic competition, 200 attendees, Mayflower Hotel DC, includes case presentations, networking dinner, awards ceremony" |
| `{{LEARNING_GOALS}}` | What you want to know | "Was the venue good? Were meals adequate for dietary needs? Did the schedule feel rushed? Would they come back? What should we change?" |
| `{{SURVEY_PLATFORM}}` | Where it goes | "Cvent" |

## Usage Notes
- "5-7 questions max" is the magic constraint — Claude defaults to 15+ questions which kills response rates
- Specifying attendee types upfront prevents a generic one-size-fits-all survey
- Mention the platform so Claude formats appropriately

## Tips
- Add: "Include one question we should ask but probably wouldn't think to"
- Chain with: "Write the survey invitation email — short, with the link placeholder and a response deadline"
- After collecting results, use Claude to analyze open-ended responses: "Categorize these 50 responses into themes"
