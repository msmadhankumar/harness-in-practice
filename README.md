# Harness in Practice

Companion repo for the Harness in Practice (https://www.linkedin.com/feed/update/urn:li:activity:7505520097013284865/) build-log series — an AI
harness wired into GitHub Copilot and GitHub Actions, built one post at a time.

The first gate is live: `wire-presence-gate.yml` blocks a PR into `dev` unless
a WIRE spec exists for the branch. It checks presence only, not quality — see
the post for what that does and doesn't catch.

## Layout

```
.
├── AGENTS.md              # what the model must read before generating
├── CODEOWNERS             # who a gate escalates to when it fails
├── specs/
│   └── WIRE-template.md   # the shape every task spec must take
└── .github/
    └── workflows/
        └── wire-presence-gate.yml   # blocks a PR with no WIRE spec for its branch
```

## Series

Follow the write-up: each post pairs with a commit here.

1. Act 1 — Scaffolding the repo
2. Act 2 — The checks: a WIRE-presence gate as a real GitHub Actions workflow (this commit)
3. Act 3 — Review with the harness in place
4. Act 4 — What to measure once it's running
5. Act 5 — Rolling it across a second repo and team
