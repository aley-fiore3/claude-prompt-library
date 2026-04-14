---
title: "Competitive Landscape Analysis"
task: analysis
domain: [startup, business, nonprofit]
complexity: intermediate
tags: [competitive-analysis, market-research, strategy, comparison]
claude_model: opus
last_tested: 2026-04-13
---

# Competitive Landscape Analysis

## Purpose
Map out who else is doing what you're doing, how they're positioned, and where the gaps are.

## The Prompt

```
Do a competitive landscape analysis for {{MY_OFFERING}}.

My positioning: {{MY_POSITION}}

Find and compare 5-8 competitors or comparable organizations. For each:
- What they offer and who they serve
- Their key differentiator
- Pricing model (if applicable)
- Strengths I should learn from
- Weaknesses I can exploit

Then give me:
1. A positioning map — where do I fit vs. the field?
2. Underserved gaps — what is nobody doing well?
3. My strongest 2-3 differentiators based on this analysis
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{MY_OFFERING}}` | What you do | "CDFI lending + small business development in rural Colorado" |
| `{{MY_POSITION}}` | How you're different | "We combine lending with hands-on technical assistance and serve agricultural communities other CDFIs skip" |

## Usage Notes
- Opus with web search gives the most current, detailed results
- For nonprofits, "competitors" means organizations serving the same population or applying for the same grants
- Works for apps, businesses, nonprofits, and consulting practices

## Tips
- Follow up with: "Based on this analysis, write 3 positioning statements I could use in a grant application"
- Ask for a simple table view if you want to paste into a deck
- Update quarterly — the landscape shifts
