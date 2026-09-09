# Review Workflows

## Single-bill review

1. Identify provider, service, billing period, statement date, due date, and amount due.
2. Extract the supported fields from `schemas/bill-record.schema.json`.
3. Reconcile previous balance, payments/credits, new charges, and amount due.
4. Reconcile line items to the statement total where possible.
5. Flag new fees, past-due amounts, estimated readings, plan changes, discount changes, and unclear items.
6. Return findings, open questions, and human next steps. Do not recommend switching providers from one bill alone unless evidence supports it.

## Period comparison

1. Confirm periods, days per period, units, and whether both readings are actual or estimated.
2. Normalize comparable fields without overwriting raw values.
3. Compare amount, usage, effective unit rate, fixed charges, variable charges, taxes/fees, credits, and adjustments.
4. Separate usage, rate, and other effects when the source supports the calculation.
5. Annualize only recurring changes. Do not annualize one-time charges or temporary credits.
6. Explain residual differences instead of forcing them into a known category.

## Workbook audit

1. Inventory sheets, tables, named ranges, period coverage, currencies, source tabs, formulas, and outputs.
2. Identify duplicate or missing keys, unmatched joins, blank-versus-zero issues, inconsistent dates, and category drift.
3. Scan formulas for errors, shifted references, hardcoded values, circular dependencies, and calculations that suppress missing inputs.
4. Reconcile headline totals to source detail independently.
5. Test representative formulas at the beginning, middle, and end of copied ranges.
6. Report confirmed defects separately from design improvements.
7. Modify the workbook only when asked. Save changes as a new version and verify recalculation plus visual layout.

## Monthly review

1. Inventory all authorized bills and workbook periods.
2. Normalize bill records and map each source to the tracker.
3. List missing, duplicate, unmatched, late, past-due, or unreconciled items.
4. Compare current month, prior month, and relevant year-over-year period when available.
5. Identify material usage, rate, fee, discount, and subscription changes.
6. Summarize current recurring monthly cost and annualized recurring cost. Keep one-time items separate.
7. Rank recommendations and required human decisions using `docs/OUTPUT_CONTRACT.md`.

## Optimization review

1. Begin with source-backed recurring costs and actual usage.
2. Identify unnecessary overlap, low-value services, expired promotions, plan mismatch, and avoidable fees.
3. Calculate a baseline using current recurring cost, excluding one-time items.
4. Estimate each opportunity using transparent assumptions.
5. Include switching costs, taxes/fees, contract limitations, service differences, promotion duration, and post-promotion price.
6. Research current offers only when requested or required. Use primary sources and record the access date.
7. Rank options without executing them.

