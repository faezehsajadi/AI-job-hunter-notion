# AI Job Hunter (No‑Code) → Notion Job Matches + Follow‑Ups

A no‑code workflow that pulls recent job posts (Gmail alerts + job boards), filters and scores them against your resume, and saves high‑match results to a Notion database for fast daily review and follow‑up.

> Note: The included categories/queries are **examples**. Customize keywords, categories, and thresholds for your own goals.

## Read order
1) docs/setup-notion.md  
2) docs/setup-claude.md  
3) docs/setup-sources.md  
4) prompts/job-search-skill.md  
5) prompts/job-matcher-criteria.md  
6) docs/automation-daily-remote-job-sweep.md (optional)  
7) docs/architecture.md (reference)  
8) docs/trouble-shooting.md (if something breaks)  
9) templates/notion-schema.md (reference)  
10) templates/sample-daily-report.md (reference)

## What you get
- **Claude skill prompt** (copy/paste): `prompts/job-search-skill.md`
- **Public, duplicateable Notion templates** (no personal data):
  - Resume template page: https://www.notion.so/9a41c6b34758441ba70cce2aaae5da1c
  - Job Matches database template: https://www.notion.so/25db95396d364ac5999d979607549f0a
  - Tasks database template (optional, for follow‑ups): https://www.notion.so/d8d2afdbe5c44bb0a2900040b6f9989a
- **Optional automation pattern (short):** `docs/automation-daily-remote-job-sweep.md`

## Prerequisites
- Claude with integrations enabled
- Notion
- Connected sources (recommended):
  - Gmail (job alert emails, including LinkedIn alerts)
  - Indeed connector
  - ZipRecruiter connector

## Quick start
1) **Duplicate the Notion templates**
   - Duplicate the Resume page and fill it with your resume text.
   - Duplicate the Job Matches database (**do not rename properties**).
   - (Optional) Duplicate the Tasks database for follow-ups.

2) **Create the Claude skill**
   - Paste `prompts/job-search-skill.md` into your Claude skill setup.

3) **Configure placeholders**
   In `prompts/job-search-skill.md`, replace:
   - `<<YOUR_RESUME_PAGE_URL>>`
   - `<<YOUR_JOB_MATCHES_DATABASE_URL>>`
   (Optional) tune `threshold` and `lookback`.

## Daily usage
Run the skill daily (or schedule it). Review results in Notion and update `Status` (e.g., `Applied`, `Interviewing`, etc.).

## Optional: follow‑up automation
If you want follow‑up tasks created automatically when a job becomes `Applied`, see:
- `docs/automation-daily-remote-job-sweep.md`

## Customization
- Raise/lower the **score threshold** (default: 65)
- Customize keywords and categories
- Add more Notion views (New / Applied / Interviewing / By Category)

## Security & privacy
- Do **not** publish your personal resume page or private database URLs.
- Use the public templates and keep tokens/secrets inside Claude/Notion connections.

## Contact
- Open a GitHub Issue for setup questions and bugs (recommended).
- Email: a2r.sahar@gmail.com

## License
MIT