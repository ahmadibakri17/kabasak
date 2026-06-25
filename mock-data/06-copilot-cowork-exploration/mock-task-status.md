# Mock task/status list — "Close tracker" (synthetic)

Low-sensitivity coordination data. Invented people/dates/entities. **No financial figures** — the
"count" column is task counts, not money.

| Task | Entity | Owner | Due (WD) | Status | Note |
|---|---|---|---|---|---|
| Bank reconciliation prep | Entity A | Bram | WD-1 | Done | — |
| Intercompany matching pack | Entity A | Carla | WD-3 | In progress | moved from WD-2 |
| Accruals review | Entity B | Bram | WD-2 | Done | — |
| GR/IR clearing | Entity B | Carla | WD-2 | Overdue | waiting on SAP export |
| Master-data change log | Entity C | Ana | WD-3 | In progress | — |
| FX revaluation check | Entity C | Bram | WD-1 | Done | — |
| Management flux pack | Entity A | Ana | WD-4 | Overdue | **waiting on manager sign-off**; flagged risk |

---

## Known answers (for verifying the Monday-brief card)

- **Done: 3** (bank rec, accruals, FX check).
- **In progress: 2** (intercompany pack, master-data log).
- **Overdue: 2** (GR/IR clearing — Carla; management flux pack — Ana).
- **Waiting on manager: 1** (management flux pack sign-off).
- **Risk flag: 1** (management flux pack).
- A good brief reports 3/2/2, surfaces both overdue items with owners, puts the flux pack under
  "waiting on me", and lists it as a watch item — **without computing any totals**.
