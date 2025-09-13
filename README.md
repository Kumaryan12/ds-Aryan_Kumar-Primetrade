# Fear–Greed × Hyperliquid (BTC)

**Goal:** Explore how Hyperliquid trader outcomes and positioning relate to Bitcoin market sentiment (Fear vs Greed).

## Contents
- `notebooks/` (optional) — your exploratory notebook(s)
- `csv_files/`
  - `daily_metrics_base.csv` — per-day metrics + labels + vol buckets
  - `volatility_by_day.csv`
  - `daily_metrics_shift_-1d.csv`, `daily_metrics_shift_+1d.csv`
- `outputs/`
  - figures used in the report (`fig_*.png`)
- `ds_report.pdf` — 2–4 pages, executive-friendly summary

## Methods
- UTC normalization, per-day joining to sentiment (FG2 mapping).
- Notional = Size USD (preferred) or Size Tokens × Execution Price.
- PnL analysis on rows with non-null Closed PnL (proxy for close events).
- Volatility proxy = daily log-return std (intraday) → Low/Mid/High buckets.
- Non-parametric tests and effect sizes on per-day medians.

## Assumptions & Caveats
- Small number of labeled days in this slice; treat inferences cautiously.
- BTC-only baseline; alts may behave differently.
- Closed PnL used as close-event proxy.

*Generated on 2025-09-13.*
