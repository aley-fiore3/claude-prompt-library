---
title: "Hotel Event Order (EO) Review Checklist"
task: events
domain: [events, logistics]
complexity: intermediate
tags: [hotel, event-orders, banquet, catering, review, quality-check]
claude_model: opus
last_tested: 2026-04-13
---

# Hotel Event Order (EO) Review Checklist

## Purpose
Review hotel event orders (banquet event orders / BEOs) for completeness, accuracy, and potential issues before an event.

## The Prompt

```
Review the following hotel event order(s) for {{EVENT_NAME}}. Act as an experienced event operations manager.

Flag any issues in these categories:
1. **Missing information** — blank fields, TBD items, missing guarantees or counts
2. **Quantity discrepancies** — attendance numbers that don't match across EOs or the master event plan (expected attendance: {{EXPECTED_ATTENDANCE}})
3. **Timing conflicts** — tight turnarounds between events, overlapping room usage, unrealistic setup/strike windows
4. **AV & technical gaps** — missing AV documentation, unclear tech requirements
5. **Catering concerns** — missing dietary accommodations, unclear service style, no beverage counts
6. **Cost red flags** — line items without pricing, unexpected charges, missing service fees

Format your review as a prioritized list: CRITICAL (must fix before event), IMPORTANT (should fix), and NICE-TO-HAVE (minor improvements).

Event Orders:
{{PASTE_EO_CONTENT}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{EVENT_NAME}}` | Name of the event | "National Ethics Case Competition 2026" |
| `{{EXPECTED_ATTENDANCE}}` | Total expected headcount | "200 attendees" |
| `{{PASTE_EO_CONTENT}}` | The actual EO text or upload the PDF | Full EO content |

## Usage Notes
- Works best with Opus for catching subtle discrepancies
- Upload the EO as a PDF if possible — Claude reads them well
- If you have multiple EOs, include all of them so Claude can cross-reference

## Example Output
> **CRITICAL**
> - Judges Dinner EO shows 45 guests but master plan lists 52 — confirm correct count with hotel by [date]
> - Thursday lunch EO has no guaranteed count — hotel needs this 72 hours prior
>
> **IMPORTANT**
> - AV requirements for Main Ballroom reference "per separate AV order" but no AV document is attached

## Tips
- Run this prompt again after the hotel sends revised EOs to verify fixes
- Add your specific hotel contact name so Claude can draft follow-up emails
- Pair with: a "draft email to hotel contact" prompt to action the flags immediately
