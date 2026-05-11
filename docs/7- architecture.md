\# Architecture (Tree)



AI Job Hunter (No‑Code System)

├─ 0) Inputs / Sources

│  ├─ Gmail job alerts

│  │  └─ Senders: LinkedIn / Indeed / ZipRecruiter (email alerts)

│  └─ Job board connectors

│     ├─ Indeed (search + job details)

│     └─ ZipRecruiter (search)

│

├─ 1) Reference text (used for scoring)

│  └─ Notion: Resume page (plain text)

│

├─ 2) Processing layer (Claude Project + Skill)

│  ├─ Fetch postings (lookback window, e.g., last 24h)

│  ├─ Extract fields

│  │  ├─ Title

│  │  ├─ Company

│  │  ├─ Link

│  │  ├─ Location / remote signal

│  │  └─ Date found

│  ├─ Normalize + deduplicate

│  │  └─ Key: (normalized\_title, normalized\_company)

│  ├─ Categorize (exactly one)

│  │  ├─ InfoSec

│  │  ├─ Cybersecurity

│  │  ├─ Cryptography

│  │  ├─ Post‑Quantum

│  │  ├─ Smart Contract Dev

│  │  └─ Smart Contract Audit

│  ├─ Score vs resume (0–100)

│  │  ├─ Skill overlap (50)

│  │  ├─ Seniority match (20)

│  │  ├─ Tools/languages match (20)

│  │  └─ Remote/location fit (10)

│  ├─ Output A: Chat summary (all results)

│  └─ Output B: Notion write (high matches only)

│     ├─ Condition: score ≥ threshold (e.g., 65)

│     └─ Condition: not already in Notion (no duplicates)

│

├─ 3) Storage / system of record (Notion)

│  ├─ Database: Job Matches — Daily

│  │  ├─ Properties: Title, Company, Category, Score, Link, Source, Match Notes, Date Found, Status

│  │  └─ Views (examples): New / Applied / Interviewing / By Category

│  └─ (Optional) Relations

│     └─ Job Matches ↔ Tasks (for follow-ups)

│

└─ 4) Follow‑up layer (Notion Tasks) — optional

&#x20;  ├─ Database: Tasks

&#x20;  │  ├─ Properties: Task, Status, Due, Next action (+ optional prioritization fields)

&#x20;  │  └─ Views (examples): Next actions / Calendar / All tasks

&#x20;  ├─ Manual follow‑up

&#x20;  │  └─ Create a task for any job you apply to

&#x20;  └─ Automation-assisted follow‑up (customizable)

&#x20;     ├─ Trigger: Job Matches.Status → Applied

&#x20;     └─ Action: Create a follow‑up task in Tasks (default Due + Next action)

