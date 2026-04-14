---
title: "API Integration Starter"
task: coding
domain: [automation, web-dev]
complexity: advanced
tags: [api, integration, python, javascript, automation]
claude_model: sonnet
last_tested: 2026-04-13
---

# API Integration Starter

## Purpose
Generate working code to connect to an API, handle authentication, and process the response.

## The Prompt

```
Write a {{LANGUAGE}} script that integrates with the {{API_NAME}} API.

What I need it to do: {{USE_CASE}}

Include:
- Authentication setup (show me where to put my API key, don't hardcode it)
- Error handling for common failures (rate limits, auth errors, timeouts)
- A main function I can call with clear parameters
- Example usage at the bottom
- Comments explaining any non-obvious API quirks

API docs are at: {{DOCS_URL}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{LANGUAGE}}` | Programming language | "Python" |
| `{{API_NAME}}` | Which API | "Cvent" |
| `{{USE_CASE}}` | What you need | "Pull all registrants for an event and export to CSV" |
| `{{DOCS_URL}}` | Link to API docs | "docs.cvent.com/api" |

## Usage Notes
- Providing the docs URL lets Claude search and write accurate code vs. guessing
- Always say "don't hardcode the API key" or Claude might put it inline
- Works for REST, GraphQL, and webhook setups

## Tips
- Follow up with: "Add retry logic with exponential backoff"
- For complex APIs, start with: "First just get authentication working and make one test call"
- Ask Claude to generate a .env.example file alongside the script
