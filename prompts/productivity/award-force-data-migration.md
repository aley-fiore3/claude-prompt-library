---
title: "Award Force Data Export & Migration"
task: productivity
domain: [events, awards]
complexity: advanced
tags: [award-force, data-migration, export, import, porting, email, CRM]
claude_model: opus
last_tested: 2026-04-13
---

# Award Force Data Export & Migration

## Purpose
Export data from Award Force (entries, judges, scores, emails, contacts) and migrate or port it into another system — Cvent, a CRM, email platform, spreadsheet, or database.

## The Prompt

```
I need to export data from Award Force and port it to {{DESTINATION}}.

What I'm migrating: {{DATA_TYPE}}
Source: Award Force program "{{PROGRAM_NAME}}"
Destination: {{DESTINATION}}
Purpose: {{PURPOSE}}

Help me:
1. **Identify what to export** — which Award Force reports or exports contain the data I need? (entries, users, scores, communications, etc.)
2. **Map the fields** — create a field mapping table:
   | Award Force field | Destination field | Transformation needed |
   Show where fields match cleanly, where they need reformatting, and where data will be lost.
3. **Flag data quality issues** — duplicates, missing emails, inconsistent formatting, merged fields that need splitting
4. **Write the cleanup script** — Python or spreadsheet formulas to transform the export into the destination's import format
5. **Create an import checklist** — step-by-step process to load the data into {{DESTINATION}} without breaking anything
6. **Validation plan** — how to verify the import worked (record counts, spot checks, test emails)

Current data volume: {{VOLUME}}
Known issues: {{ISSUES}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{DESTINATION}}` | Where it's going | "Cvent registration / Constant Contact / Google Sheets master list" |
| `{{DATA_TYPE}}` | What you're moving | "Judge contact info and emails, entrant records with submission status, scoring history" |
| `{{PROGRAM_NAME}}` | Source program | "NECC 2025" |
| `{{PURPOSE}}` | Why you're migrating | "Building the invite list for NECC 2026 in Cvent from last year's Award Force participants" |
| `{{VOLUME}}` | How much data | "200 entrants, 45 judges, 12 categories, 3 judging rounds" |
| `{{ISSUES}}` | Known problems | "Some judges used personal emails in Award Force but need institutional emails for Cvent. Several entries have two contact people but Award Force only exported the primary." |

## Usage Notes
- Award Force exports as CSV — Claude can write cleanup scripts for the transformation
- Upload the actual export file and let Claude inspect it for field mapping
- Opus is better for complex multi-system migrations

## Example Output
> **Field Mapping: Award Force → Cvent**
> | AF: `entrant_email` | Cvent: `Email Address` | Clean — direct map |
> | AF: `entrant_name` | Cvent: `First Name` + `Last Name` | **Split needed** — AF stores as single field |
> | AF: `category` | Cvent: `Registration Type` | **Transform** — map "Undergraduate" → "Student Competitor" |
> | AF: `submission_status` | — | **No equivalent** — store in Cvent custom field or lose it |

## Tips
- Always export from Award Force BEFORE the season closes — some data is harder to access after
- Chain with: "Now write the email to last year's participants inviting them to register in Cvent for this year"
- Ask: "What data should I keep in a master spreadsheet that neither platform tracks well?"
- For recurring events: "Design a data architecture that makes this migration easier next year"
