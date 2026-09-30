# ROI Express · العائد السريع

Lite single-file (`index.html`) bilingual (AR/EN, RTL/LTR) calculator for returns on shortage cases, split equally across people. Everything is client-side; data is auto-saved to `localStorage` (`roiX.v1`).

## Features
- Shortage cases: amount, admin-expense %, include toggles, investment basis, receipt/settlement dates (segmented input, calendar, paste-detect), custom rate, duplicate, **undo delete**, case numbering, live meta line (expense value, principal, accrual period, return).
- New cases copy the previous case's expense/basis settings and auto-focus.
- People: add / batch placeholders / paste / import xlsx-csv / template, **search**, **duplicate-name highlighting**, **undo delete**.
- Settings: compounding, rounding point, expense rounding, 4 day-count rules, weekend/holidays, editable rate table (**remove year**, new year inherits last rate, missing rates flagged), margin, currency, **JSON backup/restore**, full reset.
- Report: headline total, composition bar, stats grid (cases, people, date span, avg duration, effective annual yield, return on principal, avg due per case), auto narrative, case summary table with totals & %, return-by-year chart with value labels and table, expandable ledger (expand/collapse all, state kept on re-render), people shares, assumptions, print (Ctrl/Cmd+P on report tab).
- Excel export (xlsx-js-style): 6 styled sheets (Summary, Cases, Yearly breakdown, Return by year, People, Assumptions), with title bands, real date / % cells, live `SUM` total formulas, % of total formulas, autofilters, RTL view for Arabic.

## Performance
Debounced saves (flush on page hide), rAF-batched recalculation while typing, blur limited to chrome surfaces (not every card), no re-triggered entrance animations, count-up only when the total changes.

## Entry
- `index.html` — the app. `original.html` — untouched original for reference. `images/icon.jpg` — app icon.

## Next steps
- Optional weighted (non-equal) people split.
- PDF export via print stylesheet refinement.
