---
title: "Legal Rights Research"
task: research
domain: [legal, general]
complexity: intermediate
tags: [legal, rights, research, dispute, tenant, employment]
claude_model: opus
last_tested: 2026-04-13
---

# Legal Rights Research

## Purpose
Research your legal rights and options in a specific situation — tenant disputes, employment issues, property matters, consumer complaints, etc.

## The Prompt

```
I need to understand my legal rights in this situation:

{{SITUATION}}

My state: {{STATE}}
Relevant details: {{DETAILS}}

Please research and tell me:
1. **What laws or statutes apply** — cite the specific state/federal law
2. **What my rights are** under those laws
3. **What the other party's obligations are**
4. **What deadlines or time limits I need to know about** (statutes of limitation, notice periods)
5. **What my options are** — ranked from least to most aggressive
6. **What documentation I should be gathering NOW**

Use current information — search the web for my state's specific laws.

⚠️ This is for my own research. I understand this isn't legal advice and I'll consult an attorney for anything actionable.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{SITUATION}}` | What happened | "My landlord is withholding my security deposit after I moved out. The apartment was left in good condition with photos to prove it." |
| `{{STATE}}` | Your jurisdiction | "Colorado" |
| `{{DETAILS}}` | Relevant facts | "Lease ended March 31, deposit was $2,000, no itemized deduction list received, landlord not responding to calls." |

## Usage Notes
- Opus + web search is essential — laws vary dramatically by state
- Always include your state — generic legal info can be misleading
- The "documentation I should be gathering NOW" section is often the most valuable part

## Example Output
> **Applicable Law:** Colorado Revised Statutes § 38-12-103
> Under Colorado law, landlords must return security deposits within one month of lease termination, along with an itemized written statement of deductions...
>
> **Your Options (least to most aggressive):**
> 1. Send a formal demand letter (template below) via certified mail
> 2. File a complaint with the Colorado Attorney General
> 3. File in small claims court (limit: $7,500 in Colorado)

## Tips
- After getting the research, follow up with: "Draft the demand letter based on option 1"
- Ask: "What's the strongest piece of evidence I should prioritize?"
- For employment issues, specify if you're at-will, contract, or union — it changes everything
- Save the output — it's useful context for your attorney consultation
