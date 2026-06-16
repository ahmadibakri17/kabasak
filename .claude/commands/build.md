---
description: Step-by-step execution support — produces transfer-ready artifacts for work
argument-hint: [what you're building]
---

Provide build support for: $ARGUMENTS

Process:

1. Identify the owning brief in `projects/` (ask if ambiguous; offer to create one from
   `projects/_template.md` if none exists). Read it for decisions already made — do not relitigate
   them.
2. Confirm where Ahmad currently is in the build and what "done" means for today's session.
3. Delegate to the right specialist: `power-platform-engineer` for flows, apps, Office Scripts,
   SharePoint, and Copilot Studio plumbing; `copilot-prompt-engineer` for anything the work
   Copilot will execute (prompts, instructions, agent blueprints); `python-data-engineer` for
   Python and data work; `architect` if the design itself turns out to be shaky.
4. Build HERE against mock data (`mock-data/` — create fixtures first if none exist). The output
   is a transfer-ready artifact in `deliverables/<NN-slug>/`: a one-screen prompt card, a chunked
   recipe with checkpoints, or a spec + acceptance tests with reference code. The repo is not
   reachable from work — every artifact must survive transcription from a second screen.
5. Brownfield care: anything already live at work gets captured first (Ahmad describes or exports
   it, anonymized) and a rollback path agreed before changes.

End every build session with:

- the **transfer checklist** — exactly what Ahmad carries over, in what order, and
- the **at-work verification steps** — pass/fail checks he reports back next session.

Before the session ends, update the brief: decisions made (dated), deliverables & transfer log,
open questions, next actions. If the build is being declared final, route it through
`compliance-reviewer` first.
