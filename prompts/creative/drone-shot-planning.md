---
title: "Drone Shot Planning"
task: creative
domain: [travel, photography]
complexity: intermediate
tags: [drone, photography, aerial, shot-list, planning, video]
claude_model: sonnet
last_tested: 2026-04-13
---

# Drone Shot Planning

## Purpose
Plan a drone photography/videography shoot with specific shots, settings, and logistics for a location.

## The Prompt

```
Plan a drone shoot at {{LOCATION}}.

Purpose: {{PURPOSE}}
Drone: {{DRONE_MODEL}}
Time of day: {{TIME}}
Deliverables needed: {{DELIVERABLES}}

Create a shot list with:
- Shot description (what the camera sees)
- Movement type (orbit, reveal, pull-back, top-down, tracking, dolly)
- Altitude and camera angle
- Suggested settings (if relevant to my drone)
- Duration for video clips
- Sequence order for editing

Also flag:
- Airspace restrictions (search for FAA/LAANC requirements at this location)
- Best weather conditions
- Safety considerations
- Backup shots if primary locations don't work

I want {{STYLE}} — not generic real estate aerial footage.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{LOCATION}}` | Where you're shooting | "Cathedral Rock, Sedona, AZ" |
| `{{PURPOSE}}` | What it's for | "Travel content for @aley_travels + portfolio piece" |
| `{{DRONE_MODEL}}` | Your equipment | "DJI Mini 4 Pro" |
| `{{TIME}}` | When you're shooting | "Golden hour, ~1 hour before sunset" |
| `{{DELIVERABLES}}` | What you need | "5-6 hero stills + 60-second edited video" |
| `{{STYLE}}` | Visual direction | "Cinematic, emphasizing scale and solitude — not tourist postcard shots" |

## Usage Notes
- Claude can search FAA airspace maps and LAANC requirements
- Specifying your drone model helps Claude suggest realistic settings and altitudes
- "Not generic real estate aerial" is the key constraint

## Tips
- Add: "What time does golden hour start at this location on [date]?"
- Chain with: "Write Instagram captions for the 3 best shots from this shoot"
- For video: "Create a shot sequence that tells a story with a clear beginning, middle, end"
- Always check B4UFLY app the day of — temporary restrictions change
