\# Notion Schema (Public Template)



This document defines the required Notion structure for the AI Job Hunter workflow.

Do not include personal data in public copies.



\---



\## 1) Resume Page (Reference Text)

Type: \*\*Page\*\*



Purpose: The skill reads this page and uses it as the reference text for scoring job matches.



Recommended sections:

\- Professional Summary

\- Experience

\- Core Skills (tools, protocols, languages)

\- Education

\- Certifications

\- Languages

\- Links



\---



\## 2) Database: Job Matches — Daily

Type: \*\*Database\*\*



Purpose: System of record for job matches written by the skill.



\### Required properties (names must match exactly)

\- \*\*Title\*\* — Title

\- \*\*Company\*\* — Text

\- \*\*Category\*\* — Select  

&#x20; Options (must match exactly):

&#x20; - InfoSec

&#x20; - Cybersecurity

&#x20; - Cryptography

&#x20; - Post-Quantum

&#x20; - Smart Contract Dev

&#x20; - Smart Contract Audit

\- \*\*Score\*\* — Number (0–100)

\- \*\*Link\*\* — URL

\- \*\*Source\*\* — Select  

&#x20; Options (must match exactly):

&#x20; - LinkedIn

&#x20; - Indeed

&#x20; - ZipRecruiter

&#x20; - Gmail Alert

\- \*\*Match Notes\*\* — Text

\- \*\*Date Found\*\* — Date

\- \*\*Status\*\* — Select  

&#x20; Options (must match exactly):

&#x20; - New

&#x20; - Applied

&#x20; - Interviewing

&#x20; - Offer

&#x20; - Rejected



\### Suggested views (optional)

\- \*\*New\*\* (filter: Status = New)

\- \*\*Applied\*\* (filter: Status = Applied)

\- \*\*Interviewing\*\* (filter: Status = Interviewing)

\- \*\*By Category\*\* (group by: Category)



\---



\## 3) Database: Tasks (Follow-ups) — optional

Type: \*\*Database\*\*



Purpose: Track follow-up actions and reminders after you apply.



\### Recommended properties

\- \*\*Task\*\* — Title

\- \*\*Status\*\* — Status (To do / Doing / Done)

\- \*\*Due\*\* — Date

\- \*\*Next action\*\* — Text

\- Optional prioritization fields (example set):

&#x20; - Area (Select)

&#x20; - Type (Select)

&#x20; - Impact (Select)

&#x20; - Urgency (Select)

&#x20; - Effort (Select)

&#x20; - Stuck? (Checkbox)

&#x20; - Unblock note (Text)

&#x20; - Needs reminder? (Checkbox)



\### Suggested views (optional)

\- Next actions

\- Calendar

\- All tasks



\---



\## 4) Relations (optional but recommended)

If you want a clean pipeline, add a relation between the two databases:

\- In \*\*Job Matches — Daily\*\*: a relation property like `Related Tasks` → Tasks

\- In \*\*Tasks\*\*: a relation property like `Job Matches` → Job Matches — Daily



This helps you avoid duplicates and keeps follow-ups connected to the original posting.

