---
title: "IP / Patent Viability Analysis"
task: analysis
domain: [legal, startup, business]
complexity: advanced
tags: [patent, IP, intellectual-property, viability, prior-art, protection]
claude_model: opus
last_tested: 2026-04-13
---

# IP / Patent Viability Analysis

## Purpose
Evaluate whether an idea, invention, or process is likely patentable and worth pursuing IP protection.

## The Prompt

```
Analyze the patent/IP viability of the following:

Invention/Idea: {{INVENTION}}
How it works: {{MECHANISM}}
What's new about it: {{NOVELTY}}
Existing alternatives: {{ALTERNATIVES}}

Evaluate:
1. **Novelty** — has this been done before? Search for prior art.
2. **Non-obviousness** — would someone skilled in this field consider this an obvious next step?
3. **Utility** — is the practical application clear and specific?
4. **Patentable subject matter** — does this fall into a patentable category (process, machine, manufacture, composition)?
5. **Freedom to operate** — are there existing patents that could block this?
6. **Commercial viability** — even if patentable, is it worth the $10-50K investment?

Search Google Patents and USPTO for relevant prior art.

Be critical. I need to know if this is worth spending money on before I talk to a patent attorney.

⚠️ This is preliminary research, not a formal patentability opinion.
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{INVENTION}}` | What it is | "A drone-mounted sensor system for detecting specific mineral compositions in soil from aerial surveys" |
| `{{MECHANISM}}` | How it works | "Combines LIDAR with spectral analysis at specific wavelengths tuned to [material]. Processes data onboard using edge computing." |
| `{{NOVELTY}}` | What's different | "Existing systems require ground sampling. This does it aerially in real-time." |
| `{{ALTERNATIVES}}` | What exists now | "Traditional soil sampling, satellite spectral analysis (lower resolution), ground-based XRF analyzers" |

## Usage Notes
- Opus + web search for prior art research
- "Be critical" is essential — Claude defaults to encouraging, which wastes money on bad patents
- This is a pre-attorney screen, not a replacement for a patentability search

## Example Output
> **Novelty: MODERATE CONCERN.** Found 3 prior art references combining aerial spectral analysis with mineral detection (US Patent 10,XXX,XXX; US Patent 9,XXX,XXX; and a 2023 paper in Remote Sensing journal). Your edge-computing component may distinguish, but the core concept has precedent...
>
> **Recommendation:** The specific wavelength tuning + onboard processing combination is your strongest claim. Before spending on a patent attorney, narrow your claims to this specific implementation rather than the broad concept.

## Tips
- Chain with: "Draft a provisional patent application outline focusing on the strongest claims"
- Ask: "What's the cheapest way to protect this while I validate the market?"
- Provisional patents buy 12 months for ~$1,500 — often smarter than jumping to a full filing
- Keep detailed lab notebooks / development logs — they establish priority dates
