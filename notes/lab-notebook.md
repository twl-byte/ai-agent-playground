# Lab Notebook

Add a dated entry every time you make a change to this repo. Newest entries at the top.

## Example — 2026-01-01 — A. Researcher
- Ran `analysis/summarize.py` for the first time; confirmed the repo and my tool are connected.
- No changes made yet — just checking the pipeline works end to end.

## 2026-09-16 — twlevengood@gmail.com
- Ran `analysis/summarize.py` and it crashed with `KeyError: 'cohort'` in `load_groups`.
- Cause: the script read `row["cohort"]`, but `data/reaction_times.csv` has no `cohort` column — the actual column is named `group`.
- Fix: changed `analysis/summarize.py` to read `row["group"]` instead. Reran the script and confirmed it now prints per-group stats (control: n=10, mean=504.7 ms; treatment: n=10, mean=430.8 ms).

<!-- Add your own entry above this line -->
