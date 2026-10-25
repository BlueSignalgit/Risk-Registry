# Offensive Defenders — Risk Register

A responsive, static cybersecurity risk register for **Offensive Defenders**, a fictional consulting firm that outsources penetration testing engagements.

**Live site:** After enabling GitHub Pages, visit https://bluesignalgit.github.io/Risk-Registry/

## Project scope

Five hypothetical risks associated with third-party pentesting services:

| ID | Risk | Likelihood | Impact | Inherent score | Severity |
| --- | --- | ---: | ---: | ---: | --- |
| R001 | Penetration testing outside authorized scope | 3 | 5 | 15 | High |
| R002 | Leakage of client company data | 4 | 5 | 20 | Critical |
| R003 | Compromised pentester accounts or devices | 3 | 5 | 15 | High |
| R004 | Insufficient vetting of outsourced testers | 3 | 4 | 12 | Medium |
| R005 | Late or inaccurate assessment reports | 3 | 4 | 12 | Medium |

All ratings are illustrative, not the result of a real client assessment.

## Features

- Dashboard counts by severity
- Search by ID, title, category or owner
- Filter by severity and mitigation status
- Interactive 5 × 5 risk heat map
- Detailed risk descriptions, controls, impact, mitigations and owners
- Mobile-friendly dark UI

## Scoring

**Inherent risk score = Likelihood (1–5) × Impact (1–5)**.

- Low: 1–7
- Medium: 8–14
- High: 15–19
- Critical: 20–25

Likelihood values: 1 Rare; 2 Unlikely; 3 Possible; 4 Likely; 5 Almost Certain.

Impact values: 1 Negligible; 2 Minor; 3 Moderate; 4 Major; 5 Severe.

Scores are illustrative initial estimates, intended for validation during actual risk assessments. Residual risk has not been assessed.

## Run locally

From the repository root:

```bash
python -m http.server 8000
```

Visit http://localhost:8000. Opening index.html as a local file may prevent JSON loading in some browsers.

## Deploy to GitHub Pages

1. Open **Settings → Pages** in the GitHub repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select **main** and **/(root)**, then **Save**.
4. When GitHub completes deployment, visit https://bluesignalgit.github.io/Risk-Registry/

GitHub Pages settings may require appropriate repository permissions.

## Edit risks

Update `data/risks.json`. The dashboard automatically calculates inherent scores from each entry's likelihood and impact. Do not place real client reports, scopes, credentials, or security findings in this public repository.

## Disclaimer

This repository is a **fictional, educational demonstration**, not an actual risk assessment, security certification, or representation of a real client engagement.
