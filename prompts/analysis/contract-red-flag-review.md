---
title: "Contract / Agreement Red Flag Review"
task: analysis
domain: [legal, business, general]
complexity: intermediate
tags: [contract, legal, review, red-flags, negotiation]
claude_model: opus
last_tested: 2026-04-13
---

# Contract / Agreement Red Flag Review

## Purpose
Review a contract, lease, agreement, or MOU for problematic clauses, missing protections, and negotiation opportunities.

## The Prompt

```
Review this {{DOCUMENT_TYPE}} as if you were a careful attorney doing a first-pass review for a client.

My role in this agreement: {{MY_ROLE}}
The other party: {{OTHER_PARTY}}
My main concerns: {{CONCERNS}}

Flag:
1. **Red flags** — clauses that are unusually one-sided, punitive, or could cause problems
2. **Missing protections** — things that should be in here for my benefit but aren't
3. **Vague language** — terms that are ambiguous and could be interpreted against me
4. **Financial exposure** — anywhere I could owe money, penalties, or damages
5. **Exit risks** — what happens if I need to terminate, and what it costs me

For each flag, quote the specific clause, explain why it matters in plain English, and suggest what I should ask to change.

⚠️ Reminder: You're not my lawyer and this isn't legal advice. I'll have an attorney review anything before signing.

Document:
{{PASTE_DOCUMENT}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{DOCUMENT_TYPE}}` | What it is | "commercial lease" |
| `{{MY_ROLE}}` | Your position | "Tenant / lessee" |
| `{{OTHER_PARTY}}` | Who you're dealing with | "Property management company" |
| `{{CONCERNS}}` | What worries you | "Early termination costs, personal guarantee, maintenance responsibilities" |
| `{{PASTE_DOCUMENT}}` | The contract text | Full text or upload PDF |

## Usage Notes
- Opus is significantly better at catching subtle legal issues
- Upload the PDF — Claude reads them well and catches things you'd miss scrolling
- Always include the "not legal advice" reminder — this is a first-pass tool, not a replacement for an attorney

## Example Output
> **RED FLAG — Section 8.3 (Personal Guarantee):**
> "Tenant shall be personally liable for all obligations..." This means your personal assets are on the hook, not just the business. Ask to limit the guarantee to 6 months' rent or remove it entirely.
>
> **MISSING — No force majeure clause.** If something outside your control prevents use of the space, you're still on the hook for rent.

## Tips
- Run this BEFORE your attorney reviews — you'll have better questions for them
- Follow up with: "Draft a response email to the other party requesting changes to the top 3 red flags"
- For renewals, compare old vs. new: "What changed between these two versions?"
