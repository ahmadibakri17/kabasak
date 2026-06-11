---
description: Run the team's 5-step workflow — discovery → options → recommendation → plan → compliance sign-off
argument-hint: [idea or project]
---

Run the full planning workflow on: $ARGUMENTS

Follow the team's default workflow from CLAUDE.md, strictly in order:

1. **Discovery first.** Check `projects/` for an existing brief and
   `projects/01-automation-inventory.md` for related live automations. Then ask up to five sharp
   questions (volumes, current process, data sources, actors, pain) and **wait for the answers** —
   never design on assumptions.
2. **Options.** 2–3 approaches with honest trade-offs (licensing, limits, maintenance, risk). The
   simplest thing that works is always option 1. Bring in `architect` for the design thinking.
3. **Recommendation.** One option, with reasoning.
4. **Execution plan.** Milestones, human-in-the-loop checkpoints, test strategy, rollback, and
   what gets handed to which engineer.
5. **Compliance sign-off.** Send the recommended design to `compliance-reviewer` and include the
   verdict (or its conditions) in the output.

Finish by creating or updating the project brief in `projects/` (from `projects/_template.md` if
new): decisions with dates, open questions, next actions, compliance verdict.
