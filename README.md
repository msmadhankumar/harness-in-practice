# Harness in Practice

Companion repo for the [Harness in Practice](../../) build-log series — an AI
harness wired into GitHub Copilot and GitHub Actions, built one post at a time.

No checks run yet. This is the scaffold from Act 1: the repo the harness will
live in, before the first gate is written.

## Layout

```
.
├── AGENTS.md              # what the model must read before generating
├── CODEOWNERS             # who a gate escalates to when it fails
├── specs/
│   └── WIRE-template.md   # the shape every task spec must take
└── .github/
    └── workflows/         # gates land here, starting with Act 2
```

## Series

Follow the write-up: each post pairs with a commit here.

1. Act 1 — Scaffolding the repo (this commit)
2. Act 2 — The checks: a WIRE-presence gate as a real GitHub Actions workflow
3. Act 3 — Review with the harness in place
4. Act 4 — What to measure once it's running
5. Act 5 — Rolling it across a second repo and team
