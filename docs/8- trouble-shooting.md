# Troubleshooting (Quick)

Use this page if the workflow runs but results are missing, noisy, or not saved to Notion.

---

## 1) No results found
**Symptoms:** Chat summary shows 0 postings (or very few).

**Checks:**
- Gmail: Are job alert emails arriving (Inbox/Promotions/Spam)?
- LinkedIn: Are alerts enabled and being emailed to Gmail?
- Indeed / ZipRecruiter: Are connectors connected and returning results?
- Keywords: Try broader role keywords or remove overly strict filters.
- Lookback window: Increase from 24h to 48–72h temporarily.

---

## 2) Results are too noisy / irrelevant
**Symptoms:** Many low-quality or unrelated jobs.

**Fixes:**
- Reduce keywords to 5–15 high-signal terms (role titles + hard skills).
- Avoid generic terms alone (e.g., `security` without qualifiers).
- Add must-have constraints in your resume/criteria text (tools, domains).
- Raise the score threshold (e.g., 65 → 75).

---

## 3) Claude shows matches but Notion DB has no new rows
**Symptoms:** Chat summary includes jobs with high scores, but Notion stays unchanged.

**Checks:**
- Placeholders: `<<YOUR_JOB_MATCHES_DATABASE_URL>>` is correctly replaced.
- Notion connection: Claude has access to that database.
- Property names: the Job Matches database matches the template exactly:
  - `Title`, `Company`, `Category`, `Score`, `Link`, `Source`, `Match Notes`, `Date Found`, `Status`
- Threshold: jobs below threshold are not written.

---

## 4) Notion write fails with property/schema errors
**Symptoms:** Errors about missing/invalid properties.

**Fixes:**
- Do not rename database properties (keep template names).
- Ensure select options exist exactly:
  - Category: `InfoSec`, `Cybersecurity`, `Cryptography`, `Post-Quantum`, `Smart Contract Dev`, `Smart Contract Audit`
  - Source: `LinkedIn`, `Indeed`, `ZipRecruiter`, `Gmail Alert`
  - Status: `New`, `Applied`, `Interviewing`, `Offer`, `Rejected`

---

## 5) Duplicate entries keep appearing
**Symptoms:** The same job appears multiple times.

**Fixes:**
- Ensure dedup is enabled (Title + Company).
- Normalize company/title manually if needed (e.g., `Inc.` vs no suffix).
- Avoid overlapping schedules or increase lookback consistency.

---

## 6) Scoring feels wrong
**Symptoms:** Strong matches get low scores, weak matches get high scores.

**Fixes:**
- Improve resume text: add concrete tools/skills/keywords you actually have.
- Add a short “Core focus” section (3–6 lines) with your target domains.
- Tune threshold and keyword hygiene.

---

## 7) Scheduled runs miss postings
**Symptoms:** Some days you miss alerts.

**Fixes:**
- Run twice daily (optional) OR increase lookback to 48h.
- Confirm time zones and schedule time.

---

## Quick checklist (60 seconds)
- Can I open the Resume page URL?
- Can Claude access the Job Matches database?
- Are property names/options identical to the template?
- Are job alerts actually arriving in Gmail?
- Is the threshold too high?

---

## Contact
- Open a GitHub Issue for setup questions and bugs (recommended).
- Email: a2r.sahar@gmail.com