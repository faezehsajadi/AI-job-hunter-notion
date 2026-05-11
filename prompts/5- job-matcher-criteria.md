# Job Matcher Criteria (Public Template)

Use this file to define what “high match” means for **you**.  
You can paste this into your Claude project notes (or keep it in the repo and reference it when tuning the skill).

> This is intentionally generic. Replace placeholders with your own preferences.

---

## Target roles (titles)
**Primary:**
- <<ROLE_TITLE_1>>
- <<ROLE_TITLE_2>>
- <<ROLE_TITLE_3>>

**Secondary (nice-to-have):**
- <<ROLE_TITLE_4>>
- <<ROLE_TITLE_5>>

---

## Domains / categories (pick what you care about)
Select which categories you want to prioritize:
- [ ] InfoSec
- [ ] Cybersecurity
- [ ] Cryptography
- [ ] Post-Quantum
- [ ] Smart Contract Dev
- [ ] Smart Contract Audit

---

## Must-have skills (hard requirements)
A job is a **low match** if it misses these:
- <<MUST_HAVE_SKILL_1>>
- <<MUST_HAVE_SKILL_2>>
- <<MUST_HAVE_SKILL_3>>

---

## Nice-to-have skills
- <<NICE_TO_HAVE_1>>
- <<NICE_TO_HAVE_2>>
- <<NICE_TO_HAVE_3>>

---

## Seniority & role type
- Preferred level: <<Junior / Mid / Senior / Lead / Research>>
- Preferred track:
  - [ ] Industry / Engineering
  - [ ] Research / Academia
  - [ ] Either

---

## Location / remote preferences
- Remote: <<Preferred / Required / Optional>>
- Hybrid: <<OK / Not OK>>
- On-site: <<Only if city/country matches / Not OK>>
- Relocation/travel: <<Open / Not open / Case-by-case>>

---

## Red flags (auto-downscore or skip)
Skip or heavily downscore if:
- Requires clearance / citizenship you don’t have
- Unpaid / scam-like postings
- Role mismatch (e.g., pure IT support when you want security engineering)
- Missing a real company name or a valid posting link
- Very senior requirements you cannot meet (e.g., 10+ years) unless you explicitly want those

---

## Scoring policy (recommended defaults)
- Threshold to save into Notion: **65**
- Raise to **75** if results are too noisy
- Lower to **55–60** if results are too sparse

---

## Notes you want saved with each match (optional)
- What to highlight when you apply (1–2 bullets)
- What to learn / close gaps (1 bullet)
- Suggested next action (one concrete step)