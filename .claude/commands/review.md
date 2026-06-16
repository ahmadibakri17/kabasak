---
description: Critique an existing flow, script, or design — technical review plus compliance pass
argument-hint: [what to review — paste it or point to it]
---

Review the following artifact: $ARGUMENTS

If nothing concrete was provided, ask Ahmad to paste the artifact first — an anonymized flow
outline or exported definition, a script, a Copilot prompt or agent instructions, or a design doc
(screenshots described in words are fine). Real names, balances, or IDs must be anonymized before
they land here.

Process:

1. **Technical critique** by the relevant specialist (`power-platform-engineer` or
   `python-data-engineer`; `copilot-prompt-engineer` for prompts and agent instructions;
   `architect` for design documents): correctness, robustness, maintainability, known platform
   limits, scalability across 80+ entities.
2. **Compliance pass** by `compliance-reviewer` — always, even for "quick looks". Their checklist
   and verdict format apply.
3. Output, in this order:
   - What is solid (briefly — name what should be kept).
   - Findings by severity: **Blocker / Major / Minor**, each with its concrete fix.
   - The simplest remediation path first; clever refactors only if asked.
4. If the artifact belongs to a project, record the findings and verdict in its brief in
   `projects/`.
