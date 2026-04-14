---
title: "Financial Assumptions Stress Test"
task: analysis
domain: [business, nonprofit, cdfi, startup]
complexity: advanced
tags: [financial, modeling, assumptions, risk, lending, budget]
claude_model: opus
last_tested: 2026-04-13
---

# Financial Assumptions Stress Test

## Purpose
Pressure-test the assumptions in a financial model, budget, or lending projection to find where it breaks.

## The Prompt

```
I have a financial model with these assumptions:
{{ASSUMPTIONS}}

Stress-test this by:
1. Identifying the 3 assumptions most likely to be wrong
2. For each, model what happens if it's 20% worse and 40% worse than projected
3. Finding the "break point" — at what level does each assumption cause the whole model to fail?
4. Suggesting one mitigation strategy per risk

Be a skeptical CFO, not an optimistic founder. I need to know where this breaks before a funder asks me.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{ASSUMPTIONS}}` | Your model's key inputs | "Loan volume: 60 loans/year at avg $40K. Default rate: 5%. Operating costs: $450K/year. Grant revenue: $200K. Earned interest: $180K. TA fee income: $70K." |

## Usage Notes
- Opus is significantly better at financial reasoning than Sonnet
- Include all your assumptions, even the ones you're confident about
- Upload the actual spreadsheet if you have one — Claude can read .xlsx

## Tips
- Follow up with: "Now write a Risk Factors section for the grant application based on this analysis"
- Ask: "Which assumption would a CDFI Fund reviewer challenge first?"
- Run this before any board presentation or funder meeting
