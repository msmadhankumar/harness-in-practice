# Harness in Practice

Companion repo for the Harness in Practice (https://www.linkedin.com/feed/update/urn:li:activity:7505520097013284865/) build-log series — an AI
harness wired into GitHub Copilot and GitHub Actions, built one post at a time.

Three gates are live on `dev`:

- `wire-presence-gate.yml` — blocks a PR unless a WIRE spec exists for the branch. Presence only, not quality.
- `single-file-diff-gate.yml` — blocks a PR whose diff touches files the spec's `Files:` line didn't declare.
- `CODEOWNERS` — routes `.github/workflows/` and `specs/` to a required reviewer. No wildcard fallback: a path not listed here has no required reviewer, even with "Require review from Code Owners" enabled.

None of them read the code for correctness — see the posts for what each one does and doesn't catch.

## Layout

```
.
├── AGENTS.md              # what the model must read before generating
├── CODEOWNERS             # who a gate escalates to when it fails (path-specific, no wildcard)
├── specs/
│   ├── WIRE-template.md   # the shape every task spec must take
│   └── <branch-name>.md   # one WIRE spec per branch, checked by the presence gate
└── .github/
    └── workflows/
        ├── wire-presence-gate.yml      # blocks a PR with no WIRE spec for its branch
        └── single-file-diff-gate.yml   # blocks a PR whose diff isn't on the spec's Files: list
```

## Series

Follow the write-up: each post pairs with a commit here.

1. Act 1 — Scaffolding the repo
2. Act 2 — The checks: WIRE-presence gate, single-file-diff gate, and path-specific CODEOWNERS (complete)
3. Act 3 — Review with the harness in place: what GitHub Copilot's own code review catches automatically, and what still needs a human reading the diff
4. Act 4 — What to measure once it's running
5. Act 5 — Rolling it across a second repo and team
