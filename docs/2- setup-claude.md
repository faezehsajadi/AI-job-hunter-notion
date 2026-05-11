# Setup — Claude (Quick)

This guide shows how to set up the **Claude Project + Skill** for this workflow using **Gmail + Indeed + ZipRecruiter + LinkedIn alerts** + **Notion**.

## Prerequisites
- Claude with tool/integration connections enabled
- Connected integrations:
  - **Gmail** (job alert emails)
  - **Indeed** (connector)
  - **ZipRecruiter** (connector)
  - **Notion**
- LinkedIn is used via **LinkedIn job alert emails** (not direct LinkedIn scraping)
  - Make sure LinkedIn job alerts are enabled and delivered to Gmail

## Steps
1) **Create a Claude Project**
   - Name: `Job Searching` (or similar)

2) **Connect tools/integrations**
   - Enable: **Notion**, **Gmail**, **Indeed**, **ZipRecruiter**
   - Confirm Gmail receives alerts from:
     - `linkedin.com`
     - `indeed.com`
     - `ziprecruiter.com`

3) **Create the Skill**
   - Skill name: `job-hunter-infosec` (or any name)
   - Paste the full skill text from: `prompts/job-search-skill.md`

4) **Set the placeholders**
   In `prompts/job-search-skill.md`, replace:
   - `<<YOUR_RESUME_PAGE_URL>>`
   - `<<YOUR_JOB_MATCHES_DATABASE_URL>>`

5) **Run it**
   Example command in the Project chat:
   - `Run job-hunter-infosec for the last 24 hours and publish high matches to Notion.`

6) **(Optional) Schedule it**
   - Schedule the skill to run daily at your preferred time
   - Keep the lookback window at 24 hours to reduce misses and duplicates

## Verify it works
- Claude produces a chat summary of all findings
- Notion receives new rows only when:
  - score ≥ threshold, and
  - the job is not a duplicate