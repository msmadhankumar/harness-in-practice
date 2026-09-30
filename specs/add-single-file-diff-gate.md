W — WHAT:
Add the single-file-diff-gate workflow: a second gate, same shape as the WIRE-presence gate, that compares the Files: line declared in a branch's WIRE spec against the PR's actual changed files and fails by name on anything undeclared.

I — INPUT:
Files: .github/workflows/single-file-diff-gate.yml, specs/WIRE-template.md, specs/add-single-file-diff-gate.md

R — RULES:
See AGENTS.md — every gate must be able to stop a PR, not just warn.

E — EXPECTED:
- .github/workflows/single-file-diff-gate.yml exists, triggers on pull_request into dev, and does not check which agent opened the PR.
- It reads the Files: line from the branch's WIRE spec and fails the check listing any diff file not on that list.
- specs/WIRE-template.md documents the Files: field under INPUT.
