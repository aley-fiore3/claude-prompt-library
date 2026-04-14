---
title: "Certification Study Guide Generator"
task: productivity
domain: [events, cvent, general]
complexity: beginner
tags: [certification, study, flashcards, exam-prep, cvent]
claude_model: sonnet
last_tested: 2026-04-13
---

# Certification Study Guide Generator

## Purpose
Turn scattered notes and documentation into an organized study guide with key facts, gotchas, and testable items for any professional certification.

## The Prompt

```
I'm studying for the {{CERT_NAME}} certification.

Here are my raw notes and key facts I've collected:
{{RAW_NOTES}}

Organize this into a study guide with:
1. **Must-Know Facts** — the non-negotiable items likely to be tested
2. **Gotchas** — tricky distinctions, things that seem similar but aren't, common wrong answers
3. **Quick-Reference Cheat Sheet** — one-line summaries I can scan before the exam

Format for mobile — short lines, easy to scroll through.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{CERT_NAME}}` | Name of certification | "Cvent Advanced" |
| `{{RAW_NOTES}}` | Your messy notes | "Advanced Rules = Optional Session, Quantity Item, Hotel Request; Waitlists = Registration + Sessions; BOGO = Threshold 0, Interval 2..." |

## Usage Notes
- Dump in everything — Claude is great at organizing messy notes
- Works for any certification, not just Cvent
- Sonnet handles this well; no need for Opus

## Tips
- Follow up with: "Quiz me on the Gotchas section — ask 10 questions"
- Ask Claude to flag which items you should double-check against official docs
- Re-run before exam day with "just give me the cheat sheet, nothing else"
