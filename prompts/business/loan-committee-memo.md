---
title: "Loan Committee Memo"
task: business
domain: [cdfi, lending, nonprofit]
complexity: intermediate
tags: [lending, loan, memo, underwriting, committee, cdfi]
claude_model: opus
last_tested: 2026-04-13
---

# Loan Committee Memo

## Purpose
Draft a loan committee memo that presents a lending decision clearly with risk analysis and recommendation.

## The Prompt

```
Draft a loan committee memo for the following request:

Borrower: {{BORROWER}}
Loan amount: {{AMOUNT}}
Purpose: {{PURPOSE}}
Term: {{TERM}}
Rate: {{RATE}}
Collateral: {{COLLATERAL}}

Borrower financials:
{{FINANCIALS}}

Structure the memo as:
1. **Executive Summary** — the ask, the recommendation, and the DSCR in 3 sentences
2. **Borrower Overview** — who they are, business history, management assessment
3. **Loan Structure** — terms, collateral, covenants
4. **Financial Analysis** — key ratios, cash flow, capacity to repay
5. **Risk Factors** — what could go wrong, ranked by likelihood
6. **Mitigants** — how each risk is addressed
7. **Mission Alignment** — how this serves our target market (for CDFI reporting)
8. **Recommendation** — approve, approve with conditions, or decline, with clear reasoning

Write for a committee of board members who understand lending but need the analysis done for them. Be balanced — don't oversell.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{BORROWER}}` | Who's borrowing | "Mountain View Bakery LLC, owned by Maria Santos, operating 3 years in rural Pueblo County" |
| `{{AMOUNT}}` | Loan size | "$75,000" |
| `{{PURPOSE}}` | What it's for | "Equipment purchase (commercial oven + refrigeration) and working capital" |
| `{{TERM}}` | Length | "5 years" |
| `{{RATE}}` | Interest rate | "7.5% fixed" |
| `{{COLLATERAL}}` | Security | "Equipment lien + personal guarantee" |
| `{{FINANCIALS}}` | Key numbers | "Revenue: $280K (2025), $220K (2024). Net income: $35K. DSCR: 1.4x. DTI: 38%. No defaults on record." |

## Usage Notes
- Opus writes much more credible financial analysis
- Include actual financials — Claude can calculate ratios and flag issues
- "Don't oversell" prevents Claude from being an advocate instead of an analyst

## Tips
- Upload the borrower's tax returns or financials as PDF for deeper analysis
- Follow up with: "What conditions should we attach to the approval?"
- Chain with: "Draft the commitment letter based on this approval"
