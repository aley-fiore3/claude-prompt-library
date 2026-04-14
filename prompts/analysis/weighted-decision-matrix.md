---
title: "Weighted Decision Matrix"
task: analysis
domain: [general, business, startup]
complexity: beginner
tags: [decision-making, comparison, matrix, strategy]
claude_model: sonnet
last_tested: 2026-04-13
---

# Weighted Decision Matrix

## Purpose
Turn a messy "I can't decide" situation into a structured comparison with weighted criteria.

## The Prompt

```
I need to decide between these options: {{OPTIONS}}

Context: {{CONTEXT}}

Build me a weighted decision matrix. First, suggest 6-8 evaluation criteria based on my situation and ask me to confirm or adjust before scoring. Weight each criterion by importance (1-5). Then score each option against each criterion (1-10) and calculate weighted totals.

Be honest in your scoring — don't default to making everything close. If one option is clearly better on a criterion, the score should reflect that.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{OPTIONS}}` | What you're choosing between | "Accept the DC policy role vs. stay at Prairie Rose vs. move to Italy and consult remotely" |
| `{{CONTEXT}}` | What matters to you | "I value mission-driven work, financial stability, proximity to family in Italy, and career growth in policy" |

## Usage Notes
- The two-step approach (suggest criteria → confirm → score) prevents Claude from guessing wrong priorities
- Works for career decisions, vendor selection, conference attendance choices, tech stack picks
- Sonnet handles this cleanly

## Tips
- After seeing results, ask: "What changes if I double the weight on [criterion]?"
- If the scores are too close, add a tiebreaker: "Which option do I regret NOT choosing in 5 years?"
- Export the matrix as a table to share with an advisor
