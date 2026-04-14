---
title: "Regulatory Comment Letter"
task: writing
domain: [policy, legal, nonprofit]
complexity: advanced
tags: [regulatory, comment, policy, federal, advocacy, rulemaking]
claude_model: opus
last_tested: 2026-04-13
---

# Regulatory Comment Letter

## Purpose
Draft a formal public comment on a proposed federal or state regulation — for rulemaking, notice-and-comment periods, or agency proceedings.

## The Prompt

```
Draft a public comment letter on the following proposed regulation:

Regulation: {{REGULATION}}
Agency: {{AGENCY}}
Federal Register / Docket #: {{DOCKET}}
Comment deadline: {{DEADLINE}}

My organization: {{ORG}}
Our position: {{POSITION}}

The letter should:
- Open by identifying the specific regulation and docket number
- State our interest (why we have standing to comment)
- Make 3-5 specific, evidence-based arguments
- Reference data, case studies, or on-the-ground experience (I'll provide below)
- Propose specific alternative language or modifications where possible
- Be professional and substantive — these get read by policy staff

Supporting evidence I can provide:
{{EVIDENCE}}

Length: {{LENGTH}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{REGULATION}}` | What's proposed | "Proposed changes to CDFI certification requirements" |
| `{{AGENCY}}` | Who issued it | "U.S. Department of Treasury, CDFI Fund" |
| `{{DOCKET}}` | Reference number | "CDFI-2026-0001" |
| `{{DEADLINE}}` | When it's due | "May 15, 2026" |
| `{{ORG}}` | Your organization | "Prairie Rose Development Corp, a certified CDFI in Colorado" |
| `{{POSITION}}` | Your stance | "Support streamlined certification renewal but oppose proposed minimum asset threshold increase" |
| `{{EVIDENCE}}` | Supporting data | "Our lending data shows 80% of our borrowers are in persistent poverty counties. The proposed $10M asset threshold would disqualify 40% of rural CDFIs nationally." |
| `{{LENGTH}}` | Target length | "2-3 pages" |

## Usage Notes
- Opus + web search to pull current regulatory context
- Specific alternative language proposals carry more weight than general objections
- Comments that include data from actual operations are highly valued by agencies

## Tips
- Search regulations.gov for the specific docket before writing
- Ask Claude to research how other organizations commented on similar proposals
- Submit well before the deadline — late comments may not be considered
- Follow up with: "Write a 1-paragraph summary I can post on LinkedIn about why we submitted this comment"
