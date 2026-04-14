---
title: "Cvent Registration Setup Audit"
task: events
domain: [events, cvent]
complexity: advanced
tags: [cvent, registration, audit, setup, configuration, event-tech]
claude_model: opus
last_tested: 2026-04-13
---

# Cvent Registration Setup Audit

## Purpose
Review a Cvent event registration configuration for errors, missed settings, and launch-readiness before going live.

## The Prompt

```
I'm about to launch registration for {{EVENT_NAME}} in Cvent. Audit my setup.

Event details:
- Event dates: {{DATES}}
- Expected registration types: {{REG_TYPES}}
- Session structure: {{SESSIONS}}
- Payment: {{PAYMENT}}
- Hotel block: {{HOTEL}}

Here's my current configuration:
{{CONFIG_DETAILS}}

Check for:
1. **Registration type logic** — are admission items, session access, and pricing rules correct for each reg type?
2. **Session setup** — are session groups, bundles, capacity limits, and waitlists configured properly?
3. **Advanced rules** — are optional sessions, quantity items, and hotel requests using the right rule types?
4. **Payment flow** — currency locked? Discount codes working? BOGO set correctly (Threshold 0, Interval 2)?
5. **Email triggers** — confirmation, waitlist, cancellation emails all assigned?
6. **Testing** — have I used test registrations to walk through each reg type path? (Remember: 100 test regs allowed)
7. **Common Cvent gotchas**:
   - Speakers sync FROM Admin but NOT to individual events
   - Hotels DO sync
   - Currency can't be changed after launch
   - Session Groups limit to one selection
   - Session Bundles allow one-click enrollment
   - Registration Prerequisites require a prior event
   - Language Selector lives in Header/Footer
   - Payment Credits auto-award to Registrants at event end
   - Waitlists work for Registration AND Sessions
   - Opt-out is event-level only

Flag anything I might have missed. Be thorough — I'd rather catch it now than after 50 people register.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{EVENT_NAME}}` | Event name | "National Ethics Case Competition 2026" |
| `{{DATES}}` | Event dates | "April 16-19, 2026" |
| `{{REG_TYPES}}` | Who registers | "Student Competitor ($0), Faculty Advisor ($0), Judge ($0), Guest ($75)" |
| `{{SESSIONS}}` | Session structure | "6 competition rounds (limited capacity), 2 plenary sessions, 1 awards dinner, 3 optional workshops" |
| `{{PAYMENT}}` | Payment setup | "Credit card via Cvent Pay, discount code EARLYBIRD for 20% off Guest rate" |
| `{{HOTEL}}` | Hotel block info | "Mayflower Hotel block, 2 room types, April 15-20" |
| `{{CONFIG_DETAILS}}` | Your setup notes | Paste or describe your current Cvent config |

## Usage Notes
- The "Common Cvent gotchas" list is gold for Cvent Advanced cert holders — it catches the tricky stuff
- Opus handles complex event logic better
- Run this audit at least 48 hours before launch to have time to fix issues

## Tips
- After audit, follow up with: "Generate 5 test registration scenarios I should walk through — one per reg type plus an edge case"
- Chain with: "Draft the registration confirmation email for each reg type"
- For multi-event programs: "Check that prerequisites between events are configured correctly"
- Keep a master Cvent checklist that grows with each event — ask Claude to maintain it
