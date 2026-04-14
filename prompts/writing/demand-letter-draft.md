---
title: "Demand Letter Draft"
task: writing
domain: [legal, business]
complexity: advanced
tags: [legal, demand-letter, dispute, collections, negotiation]
claude_model: opus
last_tested: 2026-04-13
---

# Demand Letter Draft

## Purpose
Draft a formal demand letter for disputes involving money, property, contract breaches, or unresolved obligations.

## The Prompt

```
Draft a demand letter for the following situation:

From: {{MY_NAME}}, {{MY_ADDRESS}}
To: {{RECIPIENT_NAME}}, {{RECIPIENT_ADDRESS}}
Date: {{DATE}}

Situation: {{SITUATION}}
Amount in dispute: {{AMOUNT}}
What I've already tried: {{PRIOR_ATTEMPTS}}
Applicable law (if known): {{LAW}}
Deadline I want to set: {{DEADLINE}}

The letter should:
- Be firm and professional — not emotional or threatening
- State the facts clearly and chronologically
- Reference the specific legal basis for my claim
- State exactly what I'm demanding (money, action, or both)
- Give a clear deadline
- State what I'll do if the demand isn't met (file in small claims, report to agency, retain counsel)
- Be sendable via certified mail

Keep it to one page. Every sentence should serve a purpose.

⚠️ I understand this is a draft for my review and possible attorney consultation, not final legal correspondence.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{MY_NAME}}` | Your name | "Alessandra Ritacco" |
| `{{MY_ADDRESS}}` | Your address | "[Your address]" |
| `{{RECIPIENT_NAME}}` | Who owes you | "ABC Property Management" |
| `{{RECIPIENT_ADDRESS}}` | Their address | "[Their address]" |
| `{{DATE}}` | Today's date | "April 13, 2026" |
| `{{SITUATION}}` | What happened | "Security deposit of $2,000 not returned within 30 days of lease end per Colorado law" |
| `{{AMOUNT}}` | What they owe | "$2,000 plus treble damages under CRS § 38-12-103" |
| `{{PRIOR_ATTEMPTS}}` | What you've tried | "Called 3 times, sent email on March 15 and April 1, no response" |
| `{{LAW}}` | Legal basis | "Colorado Revised Statutes § 38-12-103" |
| `{{DEADLINE}}` | Response deadline | "14 days from receipt" |

## Usage Notes
- Opus writes much more credible legal correspondence than Sonnet
- "Not emotional or threatening" is key — angry letters weaken your position
- Always have an attorney review before sending if the amount is significant

## Tips
- Chain with the Legal Rights Research prompt first to get the law citations
- Send via certified mail with return receipt — this creates a paper trail
- After sending, set a reminder for the deadline date to follow up
- If they respond with a partial offer, use Claude to draft a counter: "They offered $X. Draft a response accepting/rejecting and explaining why."
