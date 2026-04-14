---
title: "Stakeholder Update Email"
task: writing
domain: [nonprofit, business, events]
complexity: beginner
tags: [email, update, stakeholder, board, funder, communication]
claude_model: sonnet
last_tested: 2026-04-13
---

# Stakeholder Update Email

## Purpose
Write a concise, professional update to stakeholders (board members, funders, partners) that respects their time.

## The Prompt

```
Write a stakeholder update email.

To: {{AUDIENCE}}
From: {{MY_ROLE}}
Subject matter: {{TOPIC}}

Key updates (in order of importance):
{{UPDATES}}

Tone: {{TONE}}
Length: Under {{WORD_COUNT}} words. No filler. Every sentence should be news or an action item.

End with: {{CLOSING}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{AUDIENCE}}` | Who's reading | "Board of directors" |
| `{{MY_ROLE}}` | Your title | "Chief Development Officer" |
| `{{TOPIC}}` | What it's about | "Q1 lending activity and upcoming NECC event" |
| `{{UPDATES}}` | The actual news | "1. Closed 12 loans totaling $480K. 2. NECC logistics on track, 200 registrants confirmed. 3. Submitted CDFI Fund FA application." |
| `{{TONE}}` | How formal | "Professional but warm — these are people I work with regularly" |
| `{{WORD_COUNT}}` | Max length | "200" |
| `{{CLOSING}}` | How to end | "One clear ask: approve the revised budget at next meeting" |

## Usage Notes
- The word count constraint is essential — without it, Claude writes 400+ words
- Listing updates "in order of importance" makes Claude lead with the most newsworthy item
- Works for weekly team updates, monthly board reports, funder check-ins

## Tips
- For board emails, add: "Bold the one thing they need to act on"
- Chain with: "Now write a 2-sentence version for Slack"
- If you have multiple audiences, ask Claude to adjust the same update for each
