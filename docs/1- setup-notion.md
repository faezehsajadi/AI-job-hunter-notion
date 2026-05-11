# Setup — Notion (Quick)

This guide shows how to set up Notion so the Claude skill can write job matches and you can manage follow‑ups.

## Prerequisites
- A Notion workspace
- Duplicated templates (recommended):
  - Resume template page (Public): https://www.notion.so/9a41c6b34758441ba70cce2aaae5da1c
  - Job Matches database template (Public DB): https://www.notion.so/25db95396d364ac5999d979607549f0a
  - Tasks database template (Public DB, optional): https://www.notion.so/d8d2afdbe5c44bb0a2900040b6f9989a

---

## Step 1) Duplicate the templates
1) Open each public template link.
2) Click **Duplicate**.
3) Move the duplicated pages/databases into your preferred location.

---

## Step 2) Fill your Resume page
- Open the duplicated **Resume Template** page.
- Replace all sections with your own resume text.
- Keep it updated (the skill scores job postings against this page).

---

## Step 3) Configure the Job Matches database (do not rename properties)
In the duplicated **Job Matches — Daily** database, keep property names exactly as the template:
- `Title`, `Company`, `Category`, `Score`, `Link`, `Source`, `Match Notes`, `Date Found`, `Status`

> The Claude skill expects these names. Renaming them can break Notion writes.

---

## Step 4) (Optional) Set up follow‑up tracking in Tasks
If you want follow‑up tasks/reminders:
1) Duplicate the **Tasks** template database.
2) (Optional but recommended) Create a **Relation** between databases:
   - Job Matches → Tasks (e.g., `Related Tasks`), or
   - Tasks → Job Matches (either direction works)

---

## Step 5) (Optional) Add one simple automation
Pick one:
- **Applied → create follow‑up task**  
  When a Job Match `Status` becomes `Applied`, create a Task like:  
  `Follow up: {Title} — {Company}` (with a Due date).

- **Daily sweep task (scheduled)**  
  Create a scheduled automation in Tasks to generate a recurring `Daily Remote Job Sweep` task.

See: `docs/automation-daily-remote-job-sweep.md`

---

## Step 6) (Recommended) Keep job alert email input clean (Notion Mail / Gmail)
Since Gmail alerts are a primary input:
- Create a dedicated view/label for job alerts (LinkedIn / Indeed / ZipRecruiter).
- This reduces noise, speeds up review, and improves reliability when the skill pulls recent emails.

> Notion Mail does not create a new email address — it organizes your existing Gmail inbox.

---

## Step 7) Paste URLs into the Claude skill
You will need:
- Your duplicated **Resume page URL**
- Your duplicated **Job Matches database URL**

Paste them into `prompts/job-search-skill.md`:
- `<<YOUR_RESUME_PAGE_URL>>`
- `<<YOUR_JOB_MATCHES_DATABASE_URL>>`

---

## Verify
- Run the Claude skill once.
- Confirm:
  - A chat summary is produced
  - New rows appear in **Job Matches — Daily** only for high‑match results