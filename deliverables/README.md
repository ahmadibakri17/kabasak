# Deliverables — transfer-ready outputs

One subfolder per project, numbered like its brief: `deliverables/02-account-reconciliations/`.

## Why this folder exists

This repo is **not reachable from work**. Everything here is built to be carried across manually —
read from a second screen, typed or rebuilt on the work machine. The artifact formats exist to
make that cheap and verifiable.

## Artifact types

| Type | File pattern | What it is |
|---|---|---|
| Build recipe | `recipe-*.md` | Numbered steps with a checkpoint after each ("you should now see…"), each step small enough to transcribe |
| Prompt card | `prompt-*.md` | One-screen prompt for the work Copilot (project-specific; general-purpose cards live in `prompts/`) |
| Code spec | `spec-*.md` | Build spec + acceptance tests; at work, Cursor/Copilot regenerates the code from it |
| Reference code | `src/`, `tests/` | The implementation proving the spec works — it stays here; only the spec and tests transfer |

## Rules

- **Status header on every artifact:** `draft → transferred → verified-at-work`, with version and
  date. Status changes are recorded in the owning project brief's transfer log too.
- **Every artifact ends with an at-work verification checklist** — concrete pass/fail checks
  (control totals, row counts, known-answer tests) Ahmad runs at work and reports back.
- **Code is never retyped.** Anything beyond ~30 lines goes spec-first: transfer the spec and the
  acceptance tests, regenerate at work, verify equivalence with the tests.
- **Zero confidential data** — artifacts must be carryable in plain sight: mock examples,
  placeholder names, invented values only.
