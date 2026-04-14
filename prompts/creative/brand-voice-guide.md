---
title: "Brand Voice Guide Generator"
task: creative
domain: [startup, business, culture]
complexity: intermediate
tags: [branding, voice, tone, style-guide, messaging]
claude_model: opus
last_tested: 2026-04-13
---

# Brand Voice Guide Generator

## Purpose
Create a brand voice and tone guide from scratch, or codify an existing voice into a reusable reference.

## The Prompt

```
Create a brand voice guide for {{BRAND_NAME}}.

About the brand: {{BRAND_DESCRIPTION}}
Target audience: {{AUDIENCE}}
Core values: {{VALUES}}
Personality traits (if the brand were a person): {{PERSONALITY}}

The guide should include:
1. **Voice summary** — 3 adjectives that define how we sound, with a sentence explaining each
2. **Do / Don't examples** — 5 pairs showing the right and wrong way to say things
3. **Tone spectrum** — how the voice shifts across contexts (social media vs. formal email vs. crisis communication)
4. **Vocabulary list** — words we love, words we avoid, and our specific terminology
5. **Sample copy** — rewrite these in our voice:
   - A homepage tagline
   - A social media post announcing a new program
   - An email subject line for a newsletter

Reference brands we admire (for tone, not copying): {{REFERENCE_BRANDS}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{BRAND_NAME}}` | Your brand | "AleyTravels" |
| `{{BRAND_DESCRIPTION}}` | What it is | "A travel content brand focused on authentic cultural experiences, off-the-beaten-path itineraries, and Italian-American heritage travel" |
| `{{AUDIENCE}}` | Who you're talking to | "30-50 year old professionals who want meaningful travel, not tourist traps" |
| `{{VALUES}}` | What you stand for | "Authenticity, cultural connection, adventure with intention" |
| `{{PERSONALITY}}` | Brand-as-person | "A well-traveled friend who always knows the real spot — warm, direct, a little opinionated, never pretentious" |
| `{{REFERENCE_BRANDS}}` | Tone inspiration | "Rick Steves (approachability), Condé Nast Traveler (sophistication), Anthony Bourdain (honesty)" |

## Usage Notes
- This is a one-time investment that makes every future content prompt better
- Once you have the guide, paste the voice summary into future prompts: "Write this in our brand voice: [summary]"
- Opus captures nuance in voice better than Sonnet

## Tips
- Test the guide by asking Claude to write 3 different social posts using it — if they feel consistent, the guide works
- Add a "forbidden phrases" section for things your industry overuses
- Revisit annually or after a major brand pivot
