---
title: "Beyond-the-Ratings Travel Research"
task: research
domain: [travel, culture]
complexity: intermediate
tags: [travel, restaurants, food, research, recommendations, local]
claude_model: opus
last_tested: 2026-04-13
---

# Beyond-the-Ratings Travel Research

## Purpose
Get travel and food recommendations that go deeper than aggregate star ratings, which often don't reflect actual quality.

## The Prompt

```
I'm visiting {{DESTINATION}} for {{DURATION}}.

Find me {{WHAT_TO_FIND}} that locals actually love — not just tourist-friendly spots with high Google ratings. I've found that 4.5-star places are often mediocre.

For each recommendation:
- What specifically makes it worth going to
- What to order / do / see (be specific)
- Best time to go and how to avoid crowds
- Any insider tips a local would know
- Honest downsides

Skip anything that feels like it optimizes for Instagram over substance.

My preferences: {{PREFERENCES}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{DESTINATION}}` | Where you're going | "Old Town Scottsdale, AZ" |
| `{{DURATION}}` | How long | "a full Saturday" |
| `{{WHAT_TO_FIND}}` | What you want | "restaurants and food experiences" |
| `{{PREFERENCES}}` | Dietary or style preferences | "Histamine-friendly options appreciated. No coconut, almonds, peanuts, corn, soy, tomato, garlic, or onion." |

## Usage Notes
- Works best with web search enabled so Claude pulls current info
- Adding your dietary restrictions upfront saves a round-trip of "oh wait, I can't eat that"
- Ask for a walking route if you want an efficient food tour

## Tips
- Follow up with: "Now plan a walking route that hits 5-6 of these in order, ~3 miles total"
- Ask Claude to search for recent reviews (last 6 months) rather than relying on training data
- If a rec sounds too generic, push back: "That sounds like a tourism board answer. What would a local actually say?"
