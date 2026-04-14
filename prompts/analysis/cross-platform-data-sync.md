---
title: "Cross-Platform Event Data Sync"
task: analysis
domain: [events, cvent, awards]
complexity: advanced
tags: [data-sync, cvent, award-force, migration, deduplication, cross-platform]
claude_model: opus
last_tested: 2026-04-13
---

# Cross-Platform Event Data Sync

## Purpose
Reconcile and sync data across multiple event platforms (Award Force, Cvent, spreadsheets, email tools) when running a program that spans systems.

## The Prompt

```
I'm running {{EVENT_NAME}} across multiple platforms and need to sync data between them.

Platforms in use:
{{PLATFORMS}}

What lives where:
{{DATA_MAP}}

Problems I'm seeing:
{{PROBLEMS}}

Help me:
1. **Audit the data landscape** — where is the source of truth for each data type? Flag where the same data lives in multiple places with no clear master.
2. **Find the gaps** — what data exists in one system but not the others? What's out of sync?
3. **Deduplication plan** — how to identify and merge duplicate contacts across platforms (matching on email, name, organization)
4. **Build a sync workflow** — a repeatable process for keeping data consistent:
   - What gets exported from where, and how often
   - What transformations happen in between
   - What gets imported into where
   - Who owns each step
5. **Create a master reconciliation spreadsheet** — the column structure for a single view that pulls from all platforms
6. **Post-event merge** — how to combine all data into one clean archive after the event

Write me the actual formulas or scripts for the transformations, not just descriptions.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{EVENT_NAME}}` | Event | "NECC 2026" |
| `{{PLATFORMS}}` | All systems | "Award Force (submissions & judging), Cvent (registration & hotel), Google Sheets (master tracking), Constant Contact (email campaigns)" |
| `{{DATA_MAP}}` | What's where | "Entrant names/teams in Award Force. Attendee registration in Cvent. Judge emails in both Award Force AND Cvent. Hotel blocks in Cvent. Communication history in Constant Contact. Budget in Google Sheets." |
| `{{PROBLEMS}}` | Current issues | "Judge list in Award Force doesn't match Cvent registration — 8 judges registered in Cvent but not added to AF. 3 team advisors changed email addresses between submission and registration. Some entrants registered as 'Guest' in Cvent instead of 'Student Competitor'." |

## Usage Notes
- This is the "glue" prompt for complex events that span multiple platforms
- Upload exports from each platform and let Claude cross-reference
- Opus handles multi-system logic much better than Sonnet

## Tips
- Do this reconciliation at least 2 weeks before the event, not the night before
- Chain with: "Write the email to the 8 judges who are in Cvent but not Award Force, asking them to complete their AF profile"
- Ask: "Design a single intake form that collects everything both platforms need, so next year we only enter data once"
- For post-event: "Merge everything into a single archive with one row per person and all their touchpoints"
