---
title: "Cvent Troubleshooting & Fix Finder"
task: productivity
domain: [events, cvent]
complexity: intermediate
tags: [cvent, troubleshooting, fix, debug, configuration, support]
claude_model: sonnet
last_tested: 2026-04-13
---

# Cvent Troubleshooting & Fix Finder

## Purpose
Diagnose and fix Cvent configuration issues when something isn't working as expected.

## The Prompt

```
I'm having an issue in Cvent:

**What should happen:** {{EXPECTED}}
**What's actually happening:** {{ACTUAL}}
**What I've already tried:** {{TRIED}}

Event type: {{EVENT_TYPE}}
Cvent product: {{PRODUCT}} (Registration, Surveys, Events, etc.)

Walk me through the most likely causes, starting with the simplest. For each:
- What to check (exact navigation path in Cvent)
- What the setting should be
- How to fix it

If it might be a known Cvent limitation, tell me that too so I don't waste time looking for a setting that doesn't exist.

Relevant Cvent knowledge:
- Advanced Rules types: Optional Session, Quantity Item, Hotel Request
- Waitlists apply to Registration + Sessions
- Speakers sync FROM Admin but NOT to events
- Hotels DO sync between Admin and events
- Currency locks after launch
- Session Groups = limit one selection
- Session Bundles = one-click enrollment
- Payment Credits auto-award at event end
- Test Profile lives in User Profile
- Default timezone in User Profile > Preferences
- Rename Reg Types at Admin > Data Lists > Contact Types
- Find imports at Admin > Reporting > Recent Imports/Exports
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{EXPECTED}}` | What should work | "Registrants selecting the 'Judge' reg type should see only the Judges Dinner session, not the Student Workshop sessions" |
| `{{ACTUAL}}` | What's broken | "All sessions are visible to all reg types" |
| `{{TRIED}}` | What you've done | "Checked session visibility settings, confirmed reg types are correct" |
| `{{EVENT_TYPE}}` | Kind of event | "Multi-day academic competition with multiple attendee types" |
| `{{PRODUCT}}` | Which Cvent tool | "Cvent Registration / Event Management" |

## Usage Notes
- The built-in Cvent knowledge reference prevents Claude from guessing
- "Starting with the simplest" prevents jumping to obscure solutions
- Include exact navigation paths so you can follow along in Cvent

## Tips
- Before troubleshooting, ask: "Is this a configuration issue or a Cvent limitation?"
- Screenshot the problematic screen and describe what you see
- Chain with: "Draft a support ticket to Cvent for this issue, including all the steps I've already tried"
- Keep a running "Cvent lessons learned" doc for your next event setup
