# Mock fixtures — Cowork exploration

Synthetic, low-sensitivity content for rehearsing the three Cowork prompt cards **here** before
testing at work. All names, entities, and dates are invented (`Entity A`, generic first names).
Nothing here is real or traceable to anyone.

| Fixture | Rehearses | Planted checks |
|---|---|---|
| `mock-email-thread.md` | `prompt-thread-summarizer.md` | 2 agreed items, 3 open points (1 with **no owner**) |
| `mock-meeting-transcript.md` | `prompt-meeting-to-actions.md` | 4 actions (1 with **no owner**, 1 with **no date**) |
| `mock-task-status.md` | `prompt-manager-monday-brief.md` | 7 tasks: 3 done, 2 in progress, 2 overdue; 1 "waiting on manager"; 1 risk flag |

The "planted checks" are the known answers — use them to confirm a card's *Verify before trusting*
step actually works (e.g., the summarizer should surface exactly 3 open points and flag the
ownerless one).
