# NIS2 Readiness Review — Kertvár Food Distribution Kft.

A NIS2 readiness review of a **fictional** medium-sized Hungarian food wholesaler. It contains a 46-question questionnaire mapped to NIS2 Articles 20 and 21, a score for each area, a ranked gap report, a risk register and a management summary.

> This is a **readiness review** for portfolio purposes, **not a NIS2 audit**. In Hungary, NIS2 audits are a regulated activity supervised by SZTFH.

## Why this project
NIS2 (EU Directive 2022/2555) is implemented in Hungary by **Act LXIX of 2024**, which took effect in January 2025. It covers medium and large companies in critical sectors, and many of them have no security staff. This project shows the work a junior GRC or IT audit analyst would do for such a company: turn the legal requirements into concrete checks, find the gaps, and explain to management what to fix first.

## The company (fictional)
**Kertvár Food Distribution Kft.** is a food wholesale distributor with 140 staff and about €28M revenue, based near Budapest. Food wholesale distribution is an Annex II sector, and the company's size makes it a medium-sized enterprise, so it is in scope as an **important entity**. Full profile: [`company-profile.md`](company-profile.md).

## What's in the workbook
[`nis2-readiness-review-kertvar.xlsx`](nis2-readiness-review-kertvar.xlsx)

| Sheet | Contents |
|---|---|
| **Summary** | Scope, overall score, key findings, 90-day action plan |
| **Questionnaire** | 46 questions across 11 areas, each with an answer, weight, finding and recommendation |
| **Scores** | Score and rating per area, with a bar chart |
| **Gaps** | All gaps ranked by gap score and priority |
| **Risk register** | 12 risks with likelihood, impact, score, owner, action and target date |
| **Company** | Short company profile |
| **Method** | Scoring rules, limitations, sources |

Everything is calculated with formulas. If you change an answer in the Questionnaire, the scores, priorities and summary update automatically.

## Results
| | |
|---|---|
| Overall readiness | **26% (Weak)** |
| High-priority gaps | 22 |
| High-rated risks | 3 |
| Weakest area | Effectiveness assessment (0%) |
| Strongest area | Cryptography and encryption (63%) |

**Top findings**
1. Backups aren't protected against ransomware. The only copy is online, next to the server, and has never been restore-tested.
2. MFA is on only 2 accounts, and staff have had no phishing training.
3. There's no incident procedure, and nobody knows the NIS2 reporting deadlines (24h early warning, 72h notification).
4. Suppliers have permanent remote access with only a password.
5. Management hasn't approved security measures or completed training, which Article 20 requires.

## Method
- **Areas:** NIS2 Article 20 (management) plus Article 21(2)(a)–(j). Incident reporting is checked against Article 23.
- **Scoring:** Yes = 2, Partial = 1, No = 0, N/A is excluded. Area score = points achieved ÷ points possible.
- **Gap score:** (2 − points) × weight (1–3). High ≥ 4, Medium 2–3, Low 1.
- **Risk score:** likelihood × impact (1–5 each). High ≥ 15, Medium 8–14, Low < 8.

## Limitations
- Fictional company and self-assessment answers, with no evidence testing.
- Not a legal opinion. Detailed Hungarian control requirements (Decree 418/2024) are not mapped yet.

## Possible next steps
- Map questions to ISO 27001 Annex A controls
- Hungarian version
- A small Python tool that runs the questionnaire and generates the report

## Sources
- NIS2 Directive (EU) 2022/2555, Articles 20, 21, 23
- [Act LXIX of 2024 on the cybersecurity of Hungary](https://njt.hu/jogszabaly/en/2024-69-00-00)
