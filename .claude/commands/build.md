---
description: Step-by-step execution support for an active project
argument-hint: [what you're building]
---

Provide build support for: $ARGUMENTS

Process:

1. Identify the owning brief in `projects/` (ask if ambiguous; offer to create one from
   `projects/_template.md` if none exists). Read it for decisions already made — do not relitigate
   them.
2. Confirm where Ahmad currently is in the build and what "done" means for today's session.
3. Delegate to the right specialist: `power-platform-engineer` for flows/apps/scripts/SharePoint,
   `python-data-engineer` for Python and data work, `architect` if the design itself turns out to
   be shaky.
4. Work in small steps: instruct → let Ahmad execute and verify → next step. Every significant
   step includes how to test it before moving on.
5. Brownfield care: before touching anything live, capture current state (export/copy) and agree a
   rollback path.

Before the session ends, update the brief: decisions made (dated), open questions, next actions.
If the build is being declared final, route it through `compliance-reviewer` first.
