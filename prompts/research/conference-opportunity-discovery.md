---
title: "Conference & Opportunity Discovery Research"
task: research
domain: [nonprofit, startup, events]
complexity: intermediate
tags: [conferences, scholarships, networking, opportunities, research]
claude_model: opus
last_tested: 2026-04-13
---

# Conference & Opportunity Discovery Research

## Purpose
Find relevant conferences, fellowships, scholarships, and professional development opportunities across multiple domains.

## The Prompt

```
Research conferences, fellowships, and professional development opportunities for someone with this profile:

**Role:** {{ROLE}}
**Industries/Domains:** {{DOMAINS}}
**Location flexibility:** {{LOCATION}}
**Budget:** {{BUDGET}}
**Timeframe:** {{TIMEFRAME}}

For each opportunity found, provide:
- Name, dates, location
- Why it's a fit (specific connection to my profile)
- Cost / scholarship availability
- Application deadline
- Direct contact or application link

Prioritize opportunities that offer:
1. Scholarship or reduced-cost attendance
2. Speaking or volunteer opportunities
3. Strong networking in my specific fields

Search across: industry associations, foundation programs, government-sponsored events, and university-hosted conferences.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{ROLE}}` | Your professional title + org | "CDO at a Colorado CDFI nonprofit" |
| `{{DOMAINS}}` | All relevant fields | "CDFI/community development, AI/technology, Italian-American culture, agriculture, entrepreneurship" |
| `{{LOCATION}}` | Where you can travel | "US + Italy, prefer Colorado/DC/NYC" |
| `{{BUDGET}}` | What you can spend | "Seeking free/scholarship; can self-fund up to $500" |
| `{{TIMEFRAME}}` | When you're available | "June–December 2026" |

## Usage Notes
- Use Opus with web search enabled for best results
- This works best as a starting point — follow up with specific searches on the best finds
- Run once per quarter to stay current

## Example Output
> **Milken Institute Global Conference** — May 2026, Los Angeles
> - Fit: Policy + finance intersection matches CDFI work
> - Cost: $12,500 (but Young Leaders Program offers free attendance for emerging leaders under 40)
> - Deadline: Rolling
> - Link: milkeninstitute.org

## Tips
- After getting results, use the outreach email prompt to contact each one
- Ask Claude to rank the results by "likelihood of acceptance" given your profile
- Save results to a tracking spreadsheet with status columns
