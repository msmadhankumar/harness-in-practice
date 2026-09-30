W — WHAT:
Split CODEOWNERS from a single wildcard rule into path-specific rules, one per gate/spec directory, so a failing check routes to the owner of that path instead of one name catching everything.

I — INPUT:
Files: CODEOWNERS, specs/add-codeowners-path-gate.md

R — RULES:
See AGENTS.md — CODEOWNERS is who a failing gate escalates to. No wildcard fallback: paths outside the listed rules are intentionally left with no required reviewer, to make that gap visible rather than papered over.

E — EXPECTED:
- CODEOWNERS has one rule for .github/workflows/ and one for specs/, both routed to @msmadhankumar.
- No `*` fallback rule exists — root-level files (AGENTS.md, README.md, CODEOWNERS itself) are not covered by any rule.
- Comment in CODEOWNERS states this gap plainly instead of hiding it.
