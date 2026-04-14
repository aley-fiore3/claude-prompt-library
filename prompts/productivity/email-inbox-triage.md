---
title: "Email Inbox Triage System"
task: productivity
domain: [general, business]
complexity: beginner
tags: [email, triage, inbox-zero, productivity, time-management]
claude_model: sonnet
last_tested: 2026-04-13
---

# Email Inbox Triage System

## Purpose
Process a backlog of emails by having Claude categorize and draft responses so you can clear your inbox fast.

## The Prompt

```
I have {{NUMBER}} emails to process. Help me triage them.

For each email I share, tell me:
1. **Category:** Reply now (under 2 min) / Reply later (needs thought) / Delegate / Archive / Delete
2. **Priority:** High / Medium / Low
3. **Draft reply** (if Reply Now): Write it in under 3 sentences, matching my tone — direct, warm, no fluff.

If it's Delegate, tell me who should handle it.
If it's Reply Later, give me a one-line note on what the reply needs.

My role for context: {{ROLE}}

I'll paste emails one at a time. Go.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{NUMBER}}` | How many to process | "15" |
| `{{ROLE}}` | Your position | "CDO at a Colorado CDFI — I manage development, events, and external partnerships" |

## Usage Notes
- This turns a 45-minute inbox session into 15 minutes
- Paste the email content (not forwarding) — Claude doesn't need headers and signatures
- Sonnet is fast enough for triage — save Opus for the "Reply Later" drafts

## Tips
- Batch process: save all "Reply Now" drafts, review them in one pass, then send
- For "Reply Later" items, ask Claude to add them to your reminders
- Run this daily at a set time to prevent inbox buildup
