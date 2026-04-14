---
title: "Conference Scholarship & Attendance Outreach Email"
task: writing
domain: [nonprofit, events, startup]
complexity: beginner
tags: [email, conference, scholarship, outreach, networking, cold-email]
claude_model: sonnet
last_tested: 2026-04-13
---

# Conference Scholarship & Attendance Outreach Email

## Purpose
Draft a short, direct cold email requesting scholarship, volunteer, or discounted attendance at a conference.

## The Prompt

```
Write a very short, direct email (under 100 words in the body) requesting {{REQUEST_TYPE}} for {{CONFERENCE_NAME}}.

About me: {{YOUR_BIO}}

Why this conference matters to me: {{RELEVANCE}}

Tone: Professional but warm. No fluff. Get to the ask within the first two sentences.

Send to: {{CONTACT_INFO}}

Include a subject line.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{REQUEST_TYPE}}` | What you're asking for | "volunteer attendance or scholarship" |
| `{{CONFERENCE_NAME}}` | Full name + dates if known | "SENT Summit 2026, Denver, Sept 8-11" |
| `{{YOUR_BIO}}` | 1-2 sentence professional bio | "CDO at a Colorado CDFI focused on small business lending" |
| `{{RELEVANCE}}` | Why you want to attend | "Faith-based entrepreneurship aligns with my work building community" |
| `{{CONTACT_INFO}}` | Who to address it to | "marisa@sentventures.com" |

## Usage Notes
- The "very short" and "under 100 words" constraints are key — without them Claude writes 3x too long
- Works great with Sonnet for quick drafts
- Customize the bio each time to match the conference's focus

## Example Output
> **Subject:** Volunteer/Scholarship Inquiry — SENT Summit 2026
>
> Hi Marisa,
>
> I'm the Chief Development Officer at Prairie Rose Development Corp, a Colorado CDFI. I'd love to attend SENT Summit this September — the intersection of faith and entrepreneurship is central to my work in community development.
>
> Are there volunteer spots or scholarship opportunities available? Happy to contribute however I can.
>
> Best,
> Alessandra Ritacco

## Tips
- If no response in 5 days, use this prompt again with "write a one-sentence follow-up"
- Track all outreach in a spreadsheet to build your "10K rejections" log
- Pair with: research prompt to find the right contact before emailing
