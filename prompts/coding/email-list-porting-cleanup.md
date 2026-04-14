---
title: "Email List Porting & Cleanup"
task: coding
domain: [events, awards, business]
complexity: intermediate
tags: [email, list, cleanup, deduplication, porting, migration, CSV]
claude_model: sonnet
last_tested: 2026-04-13
---

# Email List Porting & Cleanup

## Purpose
Clean, deduplicate, and reformat an email/contact list exported from one platform for import into another.

## The Prompt

```
I exported a contact/email list from {{SOURCE}} and need to import it into {{DESTINATION}}.

Clean this data:
1. **Deduplicate** — find and merge duplicates (match on email first, then name + organization)
2. **Validate emails** — flag obviously invalid addresses (missing @, typos like .cmo, disposable domains)
3. **Standardize names** — proper case, split combined first/last name fields, handle prefixes (Dr., Prof.)
4. **Normalize organizations** — "Texas A&M", "TAMU", "Texas A & M University" should all be one
5. **Fill gaps** — where one duplicate has info the other is missing, merge the most complete record
6. **Map to destination format** — reformat columns to match {{DESTINATION}}'s required import template
7. **Flag for review** — create a separate list of records that need human review (conflicting data, unclear merges)

Source format: {{SOURCE_FORMAT}}
Destination required format: {{DEST_FORMAT}}
Total records: approximately {{COUNT}}

Write a Python script that does this and outputs two CSVs: the clean import file and the "needs review" file.

Data:
{{UPLOAD_OR_PASTE}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{SOURCE}}` | Where data came from | "Award Force judge export + Award Force entrant export" |
| `{{DESTINATION}}` | Where it's going | "Cvent registration import" |
| `{{SOURCE_FORMAT}}` | Column structure | "Name (single field), Email, Organization, Role, Category, Score (if judge)" |
| `{{DEST_FORMAT}}` | Required format | "First Name, Last Name, Email, Company, Registration Type, Custom Field: Previous Role" |
| `{{COUNT}}` | How many records | "250" |
| `{{UPLOAD_OR_PASTE}}` | The data | Upload CSV |

## Usage Notes
- Upload the actual CSV — Claude will inspect it and handle edge cases you didn't anticipate
- The "needs review" output is critical — automated merges can be wrong
- Sonnet handles data cleaning scripts well

## Example Output
> **Dedup Results:**
> - 250 records in → 218 unique contacts out
> - 24 duplicates merged (same email, different name formatting)
> - 8 flagged for review (same name, different emails — could be same person or different)
>
> **Validation:**
> - 3 invalid emails flagged: jsmith@tamu.cmo, @gmail.com, test@test.test
> - 12 records missing organization — added to review list

## Tips
- Run this EVERY time you port a list — even "clean" exports have issues
- Chain with: "Now segment this list by role (judge, entrant, advisor) and create separate import files for each Cvent registration type"
- Save the Python script — you'll reuse it for every event cycle
- Ask: "What columns should I add to my master list that neither platform exports but I'll wish I had later?"
