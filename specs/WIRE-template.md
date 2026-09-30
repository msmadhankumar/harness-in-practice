# WIRE Template
# One WIRE file per feature branch, named after the branch.
# A presence-gate checks that this file exists for a task. It does not check quality.
# A diff-scope gate compares the Files: line below against the PR's actual changed files.

W — WHAT:
<!-- What exactly needs to be built or changed? -->

I — INPUT:
<!-- Which files, context, or examples are relevant? -->
Files: <!-- comma-separated list of files this change is allowed to touch, e.g. src/checkout/rateLimiter.ts, src/checkout/rateLimiter.test.ts -->

R — RULES:
<!-- Which constraint file applies? Usually a pointer (e.g. "see AGENTS.md"), not a paragraph. -->

E — EXPECTED:
<!-- What does a correct output look like? Define "done" before generation starts. -->
