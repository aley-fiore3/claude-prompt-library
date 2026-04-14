---
title: "Pitch Deck Narrative Arc"
task: creative
domain: [startup, business, nonprofit]
complexity: advanced
tags: [pitch, deck, presentation, storytelling, startup, funding]
claude_model: opus
last_tested: 2026-04-13
---

# Pitch Deck Narrative Arc

## Purpose
Build the story structure for a pitch deck before designing slides — nail the narrative, then make it pretty.

## The Prompt

```
I'm building a pitch deck for {{WHAT_FOR}}.

Audience: {{AUDIENCE}}
Goal: {{GOAL}}
Time limit: {{TIME}}

Build me a narrative arc — not slide titles, but the STORY I'm telling. Structure it as:

1. **The Hook** — the opening moment that makes them lean in
2. **The Problem** — what's broken, who's hurting, why it matters NOW
3. **The Insight** — what do we see that others miss?
4. **The Solution** — what we built/do, explained in one sentence first, then expanded
5. **The Proof** — traction, data, testimonials, anything that proves this works
6. **The Vision** — where this goes if it succeeds
7. **The Ask** — exactly what we need and what they get

For each section, write the actual words I should say (not bullet points). Keep it conversational — this is a spoken narrative, not a document.

Key facts to weave in: {{KEY_FACTS}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{WHAT_FOR}}` | The venture/initiative | "Fit Alchemy Club, a workout app combining multiple fitness disciplines" |
| `{{AUDIENCE}}` | Who you're pitching | "Angel investors at a Denver pitch competition" |
| `{{GOAL}}` | What you want | "$150K seed round" |
| `{{TIME}}` | How long you have | "5 minutes" |
| `{{KEY_FACTS}}` | Must-include data | "3,000 waitlist signups, 85% retention in beta, partnership with 2 Denver studios" |

## Usage Notes
- Story first, slides second — this prompt gets the narrative right before you touch PowerPoint
- Opus is dramatically better at storytelling structure than Sonnet
- "Write the actual words" prevents Claude from giving you bullet-point outlines

## Tips
- After getting the narrative, follow up with: "Now turn each section into a slide title + 3 bullet points max"
- Practice out loud — if any section feels clunky when spoken, ask Claude to rewrite just that part
- For Shark Tank / competition style: add "I need a memorable one-liner I can close with"
