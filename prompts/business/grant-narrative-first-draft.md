---
title: "Grant Narrative First Draft"
task: business
domain: [nonprofit, cdfi, grants]
complexity: intermediate
tags: [grant, narrative, funding, nonprofit, writing]
claude_model: opus
last_tested: 2026-04-13
---

# Grant Narrative First Draft

## Purpose
Generate a strong first draft of a grant narrative section, calibrated to funder priorities.

## The Prompt

```
Write a {{WORD_COUNT}}-word grant narrative for the following:

Applicant: {{ORG_NAME}} — {{ORG_DESCRIPTION}}
Grant program: {{GRANT_NAME}}
Funder priorities: {{FUNDER_PRIORITIES}}
Section to write: {{SECTION}}
Key data points to include: {{DATA_POINTS}}

Write in first-person plural ("we"). Be specific — use numbers, names, and concrete outcomes. Avoid jargon and buzzwords. Every sentence should either prove need, demonstrate capacity, or project impact.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{WORD_COUNT}}` | Target length | "500" |
| `{{ORG_NAME}}` | Your organization | "Prairie Rose Development Corp" |
| `{{ORG_DESCRIPTION}}` | One-liner | "A Colorado CDFI focused on small business lending in rural communities" |
| `{{GRANT_NAME}}` | Specific program | "CDFI Fund Financial Assistance Award" |
| `{{FUNDER_PRIORITIES}}` | What they care about | "Serving persistent poverty counties, measurable job creation, leverage ratio" |
| `{{SECTION}}` | Which part | "Community Need & Impact" |
| `{{DATA_POINTS}}` | Hard numbers | "47 loans closed in 2025, $2.3M deployed, 12 rural counties served, 89% borrower survival rate" |

## Usage Notes
- Feed in the actual RFP language for funder priorities — Claude will mirror their vocabulary
- Run the iterative refinement chain (generate → critique → refine) for best results
- Opus produces noticeably better grant writing than Sonnet

## Tips
- After drafting, ask: "Score this 1-10 on specificity, emotional pull, and funder alignment"
- Keep a running doc of your org's data points so you can paste them in fast
- Use the compression chain technique to tighten after drafting
