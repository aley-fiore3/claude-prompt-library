---
title: "Cvent Event Website & Agenda Copy"
task: writing
domain: [events, cvent]
complexity: intermediate
tags: [cvent, website, agenda, copy, event-marketing, landing-page]
claude_model: sonnet
last_tested: 2026-04-13
---

# Cvent Event Website & Agenda Copy

## Purpose
Write all the copy needed for a Cvent event website — landing page, about page, agenda, speaker bios, FAQ, and venue info.

## The Prompt

```
Write the website copy for {{EVENT_NAME}} in Cvent.

Event overview: {{OVERVIEW}}
Target audience: {{AUDIENCE}}
Registration types: {{REG_TYPES}}
Brand voice: {{VOICE}}

Write these pages:
1. **Hero section** — headline + 2-sentence hook that drives registration (this is the first thing people see)
2. **About / Overview** — what the event is, who it's for, why it matters (under 150 words)
3. **Agenda overview** — formatted as a day-by-day schedule with session names and times
4. **Speaker section** — template for speaker bios (50 words each)
5. **Venue & Travel** — hotel info, directions, parking, airport
6. **FAQ** — 8-10 common questions with short answers
7. **Registration CTA** — the button text + urgency line above it

Keep everything scannable — short paragraphs, clear headers. People decide to register in 30 seconds.

Schedule details:
{{SCHEDULE}}

Venue details:
{{VENUE}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{EVENT_NAME}}` | Event name | "National Ethics Case Competition 2026" |
| `{{OVERVIEW}}` | What it is | "A 3-day intercollegiate ethics case competition bringing together 200 students, faculty, and industry judges" |
| `{{AUDIENCE}}` | Who visits the site | "University students considering competing, faculty advisors, potential judges" |
| `{{REG_TYPES}}` | Registration options | "Student Competitor (free), Faculty Advisor (free), Judge (free), Guest ($75)" |
| `{{VOICE}}` | Tone | "Academic but energizing — this is a prestigious competition that should feel exciting, not stuffy" |
| `{{SCHEDULE}}` | Day-by-day | Full schedule |
| `{{VENUE}}` | Location details | "The Mayflower Hotel, 1127 Connecticut Ave NW, Washington DC" |

## Usage Notes
- "People decide to register in 30 seconds" is the key constraint for concise copy
- The hero section and CTA are the highest-impact pieces — get those right
- Sonnet is fine for web copy; fast turnaround

## Tips
- Ask Claude to write 3 hero headline options so you can pick
- Chain with: "Now write the email invitation that links to this website"
- For returning events: "Here's last year's copy — update it for this year while keeping what worked"
- Add SEO note: "Include these keywords naturally: [ethics competition, student competition, case competition DC]"
