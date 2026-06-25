# Cowork card — thread / channel summarizer (Level 1)

| Surface | Version | Status |
|---|---|---|
| Copilot Cowork (M365) | v0.1 (2026-06-25) | draft |

## Purpose

Turn a long email thread or Teams channel into a short "where it stands" without sending or
changing anything — the safest first test of Cowork's grounding.

## Data hand-in

Point Cowork at a specific **low-sensitivity** thread or channel (scheduling, logistics, an
internal coordination topic). Not customer, close-numbers, or master-data content.

## The prompt

```text
Summarize this email thread [or Teams channel] for me. Use only what is actually in it — do not
guess or add anything that isn't there.

Give me:
1. Where it stands now, in 3–5 lines.
2. Open points still needing a decision or an answer, as a bullet list with who owns each.
3. Anything explicitly agreed, as a short list.

If something is unclear or a decision has no owner, say so instead of filling it in. Do not send,
reply, or post anything — this is read-only.
```

## Expected output

A 3–5 line status, an owned open-points list, and an agreements list — every item traceable to a
real message. No actions taken.

## Verify before trusting

- [ ] Spot-check 3 claims against the actual messages — all supported.
- [ ] No invented commitments, owners, or decisions.
- [ ] Open points without an owner are flagged as such, not guessed.

## History

- 2026-06-25 — v0.1 created. Rehearse against `mock-data/06-copilot-cowork-exploration/
  mock-email-thread.md` here, then test at work on a real low-sensitivity thread.
