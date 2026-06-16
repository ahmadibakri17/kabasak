# Mock data — synthetic only

Test inputs for everything built here. **Nothing in this folder — or anywhere in this repo — may
come from a real extract. Not even one row.**

## How to build good mock data

- **Schema-faithful:** replicating real column names and data types is fine and encouraged — the
  values are always invented. The closer the shape, the less surprises at work.
- **Scaled:** enough rows to exercise the logic (usually 50–500), nowhere near real volumes.
- **Edge cases planted deliberately:** EU decimal commas, leading zeros (`"0010"`), duplicates,
  debit/credit sign conventions (S/H), missing values, period-boundary dates, accents/umlauts in
  text fields, currency mixes.
- **Standard anonyms:** `Entity A`/`E001`…, `Vendor 0001`, `Customer C-0042`, account descriptions
  generic ("Trade receivables"), dates invented.

## Generators over hand-built files

Prefer a small seeded Python generator: `generators/make_<dataset>.py` with a fixed random seed so
datasets are reproducible. The generator doubles as documentation of the schema — and its spec can
be transferred to work to produce matching test data there (same shape, also fake) for at-work
verification runs.

## Layout

Project-specific datasets mirror the brief numbering: `mock-data/02-account-reconciliations/…`.
Shared/generic fixtures live at the top level.
