---
title: "Policy Brief Research & Drafting"
task: research
domain: [policy, federal, nonprofit]
complexity: advanced
tags: [policy, brief, legislation, advocacy, research, government]
claude_model: opus
last_tested: 2026-04-13
---

# Policy Brief Research & Drafting

## Purpose
Research a policy topic and draft a concise brief suitable for legislative staff, agency officials, or advocacy.

## The Prompt

```
Research and draft a 2-page policy brief on {{POLICY_TOPIC}}.

My position/angle: {{POSITION}}
Target reader: {{AUDIENCE}}
Relevant legislation or programs: {{LEGISLATION}}

Structure:
1. **Executive Summary** (3 sentences max)
2. **Background** — what's the current state of this policy?
3. **The Problem** — what's not working and who's affected? Use data.
4. **Policy Options** — 2-3 realistic approaches with pros/cons
5. **Recommendation** — what we advocate for and why
6. **Call to Action** — one specific thing the reader can do

Requirements:
- Use current data (search the web)
- Cite sources
- Write for someone smart but not expert in this area
- Under 800 words
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{POLICY_TOPIC}}` | The issue | "CDFI Fund appropriations and reauthorization for FY2027" |
| `{{POSITION}}` | Your stance | "Advocating for increased CDFI Fund appropriations and streamlined certification renewal" |
| `{{AUDIENCE}}` | Who reads it | "Congressional staff on the Financial Services Committee" |
| `{{LEGISLATION}}` | Related bills/programs | "Community Development Financial Institutions Act, CDFI Bond Guarantee Program" |

## Usage Notes
- Opus + web search is essential here — you need current legislative data
- "2-3 realistic approaches" prevents Claude from suggesting moonshot solutions
- Policy briefs should be shorter than you think — staffers skim

## Tips
- Follow up with: "Now write a 3-paragraph email to my representative referencing this brief"
- Ask Claude to find the relevant committee members and their positions on this issue
- Keep briefs updated as legislation moves — ask Claude to track changes
