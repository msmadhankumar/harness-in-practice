W — WHAT:
Update README.md so the Layout and Series sections match what's actually been built: the single-file-diff-gate workflow (post-04), the path-specific CODEOWNERS split (post-05), and Act 3's review-bot argument (post-06) — none of which the README currently mentions.

I — INPUT:
Files: README.md, specs/sync-readme-with-act2-act3.md

R — RULES:
See AGENTS.md — no hallucinated claims. Only document gates and settings that actually exist in this repo (wire-presence-gate.yml, single-file-diff-gate.yml, CODEOWNERS) or are native GitHub features referenced accurately (Copilot code review, Copilot approvals).

E — EXPECTED:
- Layout tree lists both workflow files and shows specs/ holding one WIRE file per branch, not just the template.
- Intro paragraph names all three live gates (presence, diff-scope, CODEOWNERS) and states plainly that none of them check code correctness.
- Series section marks Act 2 complete and adds an Act 3 line describing the review-bot argument from post-06, without claiming any new committed artifact for it.
