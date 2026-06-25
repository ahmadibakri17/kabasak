# Cowork card — manager's Monday brief (Level 3)

| Surface | Version | Status |
|---|---|---|
| Copilot Cowork (M365) | v0.1 (2026-06-25) | draft |

## Purpose

Have Cowork run a multi-step gather across a few coordination sources and compile **one** weekly
brief — lifting the "dig through five places" job off a manager. Tests multi-step planning and the
numbers boundary.

## Data hand-in

Point Cowork at **low-sensitivity coordination sources only**: a task/status list (SharePoint), a
team calendar, and an open-items or requests list. **No real financial figures** in scope for this
test.

## The prompt

```text
Build me a short Monday brief from the sources I point you to. Use only what's in them — do not
calculate or estimate anything, and quote any number exactly as it appears in the source.

Structure:
1. Close / task status — what's done, in progress, overdue (with owners), from the task list.
2. Deadlines this week — from the calendar and open-items list.
3. Things waiting on me — items needing my decision or sign-off.
4. Watch items — anything flagged as a risk in the sources.

Keep it to one screen. If a source is missing or unclear, say so. Show me the brief — don't send or
post it.
```

## Expected output

A one-screen brief in four sections, every item traceable to a source, **every number quoted not
computed**, held for your review (not sent).

## Verify before trusting

- [ ] Counts and dates match the source lists (spot-check a few).
- [ ] No number was calculated — all are quotes from a source cell/line.
- [ ] Overdue items and owners are correct; nothing invented or missed.
- [ ] Note the credit cost of the run.

## History

- 2026-06-25 — v0.1 created. Rehearse against `mock-data/06-copilot-cowork-exploration/
  mock-task-status.md` here, then test at work on low-sensitivity coordination data.
