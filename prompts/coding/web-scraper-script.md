---
title: "Quick Web Scraper Script"
task: coding
domain: [automation, web-dev]
complexity: intermediate
tags: [python, scraping, automation, data-collection]
claude_model: sonnet
last_tested: 2026-04-13
---

# Quick Web Scraper Script

## Purpose
Generate a working Python script to scrape structured data from a website.

## The Prompt

```
Write a Python script that scrapes {{TARGET_DATA}} from {{WEBSITE}}.

Requirements:
- Use requests + BeautifulSoup (no Selenium unless JS rendering is required)
- Handle errors gracefully (timeouts, missing elements, rate limiting)
- Output to {{OUTPUT_FORMAT}}
- Include a 2-second delay between requests
- Add comments explaining each step

If the site likely blocks scrapers, suggest alternatives (API, RSS, etc.) before writing the scraper.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{TARGET_DATA}}` | What to extract | "grant deadline dates and program names" |
| `{{WEBSITE}}` | Source URL | "cdfi.org/programs" |
| `{{OUTPUT_FORMAT}}` | How to save it | "CSV with columns: program_name, deadline, url" |

## Usage Notes
- Always check the site's robots.txt and terms of service first
- Claude will often suggest an API if one exists — this saves you headaches
- Sonnet is fine for straightforward scraping; use Opus for complex multi-page crawls

## Tips
- Add "make it resumable" if scraping many pages — Claude will add checkpoint logic
- For sites that need login, say "use session cookies" and Claude will structure it
- Follow up with: "Now schedule this to run weekly and email me if any deadlines are within 30 days"
