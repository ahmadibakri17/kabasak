# Excel: anomaly scan on a line-item table

| Surface | Version | Status |
|---|---|---|
| Copilot in Excel | v0.1 (2026-06-12) | draft |

## Purpose

Have Copilot in Excel flag likely data-quality issues in a transaction/GL line table before
reconciliation work starts — labeling rows only, never changing values.

## Data hand-in

The data must be a proper Excel Table (select range → **Ctrl+T**) with a single header row, e.g.
`Entity | Account | DocNo | Date | Amount | Currency`. One table per ask — no merged cells or
multi-row headers.

## The prompt

```text
Using only the data in this table, help me find data-quality issues. Do not change any existing
values.

1. Add a column "Flag" that labels rows which are: duplicates of another row (same DocNo and
   Amount), missing a value in any column, dated outside {period, e.g. 2026-05}, or have an
   Amount of exactly zero.
2. Then tell me how many rows you flagged in each category.

Only label existing rows — do not calculate any new amounts.
```

## Expected output

A new `Flag` column with category labels on affected rows, plus a count per category in the chat
pane. Row data otherwise untouched.

## Verify before trusting

- [ ] Row count unchanged after the edit.
- [ ] Control total: SUM of `Amount` identical before and after.
- [ ] Re-derive the duplicate count with `COUNTIFS` on DocNo + Amount and compare.
- [ ] Filter on `Flag` and confirm the per-category counts match what Copilot reported.

## History

- 2026-06-12 — v0.1 created as a library seed; dry-run against a mock GL extract with planted
  duplicates, blanks, and out-of-period dates before first work use.
