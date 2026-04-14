---
title: "Legal Document Plain-Language Summary"
task: analysis
domain: [legal, general]
complexity: beginner
tags: [legal, summary, plain-language, contract, lease, terms]
claude_model: sonnet
last_tested: 2026-04-13
---

# Legal Document Plain-Language Summary

## Purpose
Translate a legal document into plain English so you actually understand what you're agreeing to.

## The Prompt

```
Translate this legal document into plain English.

Document type: {{DOCUMENT_TYPE}}

For each section:
- What it says in normal human language
- What it means for ME practically
- Anything surprising or unusual compared to standard {{DOCUMENT_TYPE}} documents

Flag anything where I'm giving up rights, accepting liability, or could owe money I might not expect.

Write it so someone with zero legal background understands every word.

Document:
{{PASTE_DOCUMENT}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{DOCUMENT_TYPE}}` | What it is | "employment agreement" |
| `{{PASTE_DOCUMENT}}` | The full text | Paste or upload PDF |

## Usage Notes
- Sonnet handles this well — it's summarization, not legal analysis
- Upload the PDF rather than pasting if the formatting is complex
- Works for leases, employment agreements, terms of service, insurance policies, loan docs, NDAs

## Example Output
> **Section 4 — Non-Compete (plain English):**
> If you leave this job, you can't work for any competing company within 50 miles for 2 years.
>
> **What this means for you:** This is aggressive. In Colorado, non-competes are largely unenforceable for most employees as of 2022 (HB 22-1317), but you'd still need to challenge it if they tried to enforce.
>
> **Unusual?** Yes — the 50-mile radius and 2-year duration are both above typical.

## Tips
- After getting the summary, follow up with: "What are the 3 things I should negotiate before signing?"
- For terms of service, ask: "What am I agreeing to that most people don't realize?"
- Keep the plain-language summary alongside the original — useful reference if disputes arise later
