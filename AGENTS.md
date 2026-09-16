# AGENTS.md
# AI Agent Instructions — Harness in Practice
# Companion repo for the "Harness in Practice" build-log series

---

## FIRST ACTION — READ THESE FILES

Before generating any code in this repo, read:

1. `specs/WIRE-template.md` — the shape every task spec must take before a check will accept it
2. `CODEOWNERS` — who a failing gate escalates to

Treat every rule below as a hard constraint, not a suggestion.

---

## Project Context

This repo is the companion to the "Harness in Practice" series — a build log for
an AI harness wired into GitHub Copilot and GitHub Actions. Each post in the
series pairs with a working change here: a check, a workflow, a gate.

---

## Non-Negotiables

- Every task starts from a WIRE spec in `specs/` — no spec, no generation
- Layer boundaries and naming follow whatever `specs/WIRE-template.md` points to for the task at hand
- Do not commit commented-out code
- Do not add a check that can only warn — every gate must be able to stop a PR

---

## When You Are Unsure

If a task is ambiguous or a rule here conflicts with the WIRE spec for the task:

1. State the ambiguity explicitly
2. Ask for clarification
3. Do not assume and proceed
