
Week 3 — Descriptive analytics
NAME : ALIYAN IRFAN
ERP ID :36140
GRACE TOKEN USED : YES 

 Files included:

- `1_attempt.md` — draft referee's note with O/E/C sentence labels and data hashes
- `2_work.ipynb` — reproducible descriptive statistics and sensitivity analysis
- `3_log_reflection.md` — interpretation audit, classmate transcript excerpt and reflection
- `AI_USE_LOG

Data provenance and limitation

The source CSV labels the observations **“ILLUSTRATIVE TEACHING DATA - NOT ACTUAL PBS OBSERVATIONS.”**
The Week 1 cleaned file was recovered from the prior assignment work. The Week 2 file included here is a provisional reconstruction from the original messy CSV and the cleaning decisions documented in the available prior work. It has not yet been matched against the student's final Week 2 submission or original cleaning log. If the final Week 2 file differs, replace the provisional file and rerun the Week 2 sensitivity section in the notebook.

## Method

For each item, the mean and median use all available numeric prices across both cities. First-to-last percentage change is calculated from the average of the two city prices on the first date and the average on the last date:

`((last-date city average − first-date city average) / first-date city average) × 100`

The percentage change is a descriptive comparison between the two endpoints, not a claim about what happened on every date or why it happened.
