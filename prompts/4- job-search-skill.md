# Job Hunter — InfoSec, Cryptography & Smart Contracts (Public Skill)

**Trigger:** Slash command + scheduled run (recommended)

## Description
Use when you want a daily job-search check (e.g., “job check”, “find new jobs”, “run job hunter”), or when you want to update job tracking.

This skill:
- Aggregates recent job postings from **Gmail job alerts**, **Indeed**, and **ZipRecruiter**
- Filters + categorizes postings
- Scores each posting against the user’s **Notion resume page**
- Writes high‑match results into a **Notion Job Matches database**

> Important: The role categories and query strings in this template are **examples**.  
> Each user should customize keywords, role titles, categories, and scoring thresholds to match their own goals.

---

## Configuration (PUBLIC TEMPLATE — replace placeholders)
Set these per user:
- **Resume page URL:** `<<YOUR_RESUME_PAGE_URL>>`
- **Job Matches database URL:** `<<YOUR_JOB_MATCHES_DATABASE_URL>>`
- **Score threshold for Notion entry:** `65`
- **Lookback window:** `24 hours`
- **Accepted languages:** English, Persian (Farsi)
- **Remote preference:** prefer remote; hybrid acceptable; on-site only if compatible with the user’s preference

---

## Categories (example set — customize per user)
Each posting must map to exactly one category. This template uses an example set:
- `InfoSec`
- `Cybersecurity`
- `Cryptography`
- `Post-Quantum`
- `Smart Contract Dev`
- `Smart Contract Audit`

Users can rename/add/remove categories — but if you do, make sure your Notion `Category` select options match **exactly**.

---

## Workflow

### Step 3 — Search job-board connectors (example queries — customize per user)
Run parallel searches against Indeed and ZipRecruiter.

Example query strings (edit as needed):
- InfoSec: `information security`
- Cybersecurity: `cybersecurity`
- Cryptography: `cryptography engineer`
- Post-Quantum: `post quantum cryptography`
- Smart Contract Dev: `smart contract developer`
- Smart Contract Audit: `smart contract auditor`

For each query:
- Prefer remote filters where supported
- Lookback: last 24 hours
- No salary minimum

---

## Customization notes (recommended)
- If results are **too noisy**:
  - tighten queries (more specific role titles + hard skills)
  - raise threshold (e.g., 65 → 75)
- If results are **too sparse**:
  - broaden queries
  - lower threshold (e.g., 65 → 55–60)
- Keep Notion schema aligned:
  - Any category/source/status values written by the skill must exist as select options in Notion.