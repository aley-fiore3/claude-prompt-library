---
title: "Initiative One-Pager"
task: business
domain: [nonprofit, startup, business, policy]
complexity: intermediate
tags: [one-pager, executive-summary, pitch, overview, funding]
claude_model: opus
last_tested: 2026-04-13
---

# Initiative One-Pager

## Purpose
Distill any project, program, or venture into a single-page overview suitable for funders, board members, or potential partners.

## The Prompt

```
Create a one-pager for {{INITIATIVE_NAME}}.

What it is: {{DESCRIPTION}}
Who it serves: {{BENEFICIARIES}}
Key results so far: {{TRACTION}}
What we need: {{ASK}}
Why now: {{URGENCY}}

Requirements:
- Must fit on one page when printed (roughly 400-500 words)
- Lead with the problem, not the solution
- Include 2-3 hard numbers
- End with a clear call to action
- No jargon — a smart person outside our field should understand it immediately

Audience: {{AUDIENCE}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{INITIATIVE_NAME}}` | Name of the thing | "Prairie Rose Rural Lending Expansion" |
| `{{DESCRIPTION}}` | What it does | "Expanding CDFI lending services to 5 additional rural Colorado counties with no current access to community development financing" |
| `{{BENEFICIARIES}}` | Who benefits | "Small business owners and agricultural producers in persistent poverty counties" |
| `{{TRACTION}}` | Proof it works | "47 loans, $2.3M deployed, 89% borrower survival rate, 12 counties currently served" |
| `{{ASK}}` | What you need | "$500K in program funding + 2 new loan officers" |
| `{{URGENCY}}` | Why now | "3 rural banks closed in our service area in 2025, leaving 15,000 residents without local lending options" |
| `{{AUDIENCE}}` | Who reads this | "CDFI Fund program officers" |

## Usage Notes
- "No jargon" is the most important constraint — sector insiders forget how opaque their language is
- Opus writes significantly tighter one-pagers than Sonnet
- Have Claude create it as a Word doc if you need formatting (headers, logo space)

## Tips
- Chain with: "Now adapt this for a corporate sponsor who cares about community impact metrics"
- Test readability: "Would a congressional staffer with no CDFI background understand this in 60 seconds?"
- Keep a master one-pager updated quarterly — you'll use it constantly
