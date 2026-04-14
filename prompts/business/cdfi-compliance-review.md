---
title: "CDFI Compliance Document Review"
task: business
domain: [cdfi, nonprofit, lending]
complexity: advanced
tags: [compliance, cdfi, certification, lending, regulatory, audit]
claude_model: opus
last_tested: 2026-04-13
---

# CDFI Compliance Document Review

## Purpose
Review CDFI certification documents, annual reports, or compliance materials for completeness and potential issues before submission.

## The Prompt

```
Review this {{DOCUMENT_TYPE}} for CDFI Fund compliance.

Our CDFI details:
- Organization: {{ORG_NAME}}
- Certification type: {{CERT_TYPE}}
- Target market: {{TARGET_MARKET}}
- Primary financing activity: {{ACTIVITY}}

Review for:
1. **Completeness** — are all required sections present and filled?
2. **Target market consistency** — does everything align with our certified target market?
3. **Accountability requirements** — do we demonstrate adequate board/advisory representation from our target market?
4. **Development services documentation** — is our TA/development services activity adequately described?
5. **Financial product alignment** — do our products match what CDFI Fund expects for our certification type?
6. **Red flags** — anything that could trigger additional scrutiny or a compliance finding

Be specific about what's missing or weak. I'd rather fix it now than get a deficiency notice.

Document:
{{PASTE_DOCUMENT}}
```

## Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `{{DOCUMENT_TYPE}}` | What you're submitting | "Annual Certification and Data Collection Report (ACR)" |
| `{{ORG_NAME}}` | Your CDFI | "Prairie Rose Development Corp" |
| `{{CERT_TYPE}}` | Type | "Loan Fund" |
| `{{TARGET_MARKET}}` | Who you serve | "Low-income targeted populations in rural Colorado counties" |
| `{{ACTIVITY}}` | What you do | "Small business lending and technical assistance" |
| `{{PASTE_DOCUMENT}}` | The document | Full text or upload |

## Usage Notes
- Opus for the nuanced compliance analysis
- Upload the actual document rather than summarizing — details matter in compliance
- This works for ACRs, certification applications, AMIS data entry review, and FA (Financial Assistance) applications

## Tips
- Run this before every annual submission
- Chain with: "Draft responses to each deficiency you identified"
- Ask Claude to search for recent CDFI Fund guidance notices that might affect your submission
- Keep a compliance calendar — ask Claude to create one based on CDFI Fund deadlines
