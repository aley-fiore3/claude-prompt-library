---
title: "Social Media Content Batch Generator"
task: creative
domain: [startup, business, travel, culture]
complexity: beginner
tags: [social-media, content, instagram, linkedin, batch, scheduling]
claude_model: sonnet
last_tested: 2026-04-13
---

# Social Media Content Batch Generator

## Purpose
Generate a week's worth of social media posts in one shot, ready to schedule.

## The Prompt

```
Create {{NUMBER}} social media posts for {{PLATFORM}} for {{BRAND_OR_ACCOUNT}}.

Content pillars (rotate through these):
{{PILLARS}}

For each post:
- The caption (appropriate length for the platform)
- 3-5 hashtags (mix of niche and broader)
- Suggested image/visual description
- Best time to post (based on platform norms)

Tone: {{TONE}}
Avoid: {{AVOID}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{NUMBER}}` | How many posts | "7" |
| `{{PLATFORM}}` | Which platform | "Instagram" |
| `{{BRAND_OR_ACCOUNT}}` | Account identity | "@aley_travels — authentic Italian-American heritage travel" |
| `{{PILLARS}}` | Content themes | "1. Hidden gems in Italy, 2. Italian-American culture/food, 3. Travel tips & hacks, 4. Personal story/behind the scenes" |
| `{{TONE}}` | How it should sound | "Warm, conversational, like texting a friend who asks 'where should I eat in Rome'" |
| `{{AVOID}}` | What not to do | "Generic travel clichés, 'wanderlust', overly curated/influencer energy" |

## Usage Notes
- Sonnet is fast and good enough for social copy
- Specifying content pillars prevents Claude from writing 7 posts that all sound the same
- Include "suggested image description" so you know what visual to pair

## Tips
- Chain with: "Now adapt these for LinkedIn with a more professional angle"
- Ask Claude to create a content calendar table you can paste into a spreadsheet
- For Instagram specifically, add: "Write the first line as a hook — it's the only thing people see before 'more'"
