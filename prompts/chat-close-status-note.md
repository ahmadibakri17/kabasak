# Close status note from a task table

| Surface | Version | Status |
|---|---|---|
| M365 Copilot chat | v0.1 (2026-06-12) | draft |

## Purpose

Turn a pasted close-checklist table into a grouped status overview plus a short status note for
the manager — without Copilot inventing or recalculating anything.

## Data hand-in

Paste a task table below the prompt, with columns:
`Task | Entity | Owner | Due (WD) | Status | Comment`. Any status wording works as long as done /
in progress / blocked are distinguishable.

## The prompt

```text
You are helping a financial controller report month-end close status. Below is the current close
task list. Use ONLY the rows provided — do not invent, recalculate, or estimate anything.

1. Group the tasks into: Done, In progress, Blocked/overdue.
2. List every Blocked/overdue task with its entity, owner, and the comment given.
3. Draft a status note for my manager (max 5 sentences): overall state, how many tasks are done
   out of the total, the biggest risks, and what I need from them.

If a required column is missing or a value is unclear, say so instead of guessing.

{paste the task table here}
```

## Expected output

Three grouped lists, a complete blocked/overdue list with owners, and a ≤5-sentence note. Every
count and name in the answer must already exist in the pasted table.

## Verify before trusting

- [ ] The "done out of total" count matches your own filter/count of the table.
- [ ] Every blocked task it lists exists in the table — nothing invented, nothing dropped
      (compare counts both ways).
- [ ] Spot-check two owners and one comment against the source rows.

## History

- 2026-06-12 — v0.1 created as a library seed; dry-run it against a mock close checklist before
  first work use.
