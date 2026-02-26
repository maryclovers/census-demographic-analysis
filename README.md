# Census Demographic Analysis

**MSc AI for Healthcare — Fundamentals of Data Science | University of Hull**
**Grade: Distinction (89–91%)**

---

## What this is

A full demographic analysis of a UK census dataset — cleaning messy real-world data, running statistical tests, and pulling out insights about how this population compares to national UK averages.

Built this as part of my MSc, but the skills here (handling missing data, imputation strategies, significance testing, visualisation) are exactly what you'd do on a clinical data pipeline before any ML model touches it. Garbage in, garbage out — this project is about making sure the data is actually trustworthy before you do anything with it.

---

## What I actually did

**Data Cleaning**
- Found and fixed missing values in Age (median imputation) and Religion (mode imputation)
- Flagged impossible ages (negative values, ages over 122) and replaced with median
- Caught logical inconsistencies: people listed as married under 18, children in work categories — fixed or flagged each one with justification
- Validated invalid religion entries against a known list, categorised outliers as "Other"

**Analysis**
- Age distribution, gender split, marital status breakdown, religion distribution
- Household size analysis (grouped by street + house number)
- Occupation breakdown — identified unusually high student population
- Estimated birth rate and death rate from cohort data

**UK Comparison + Stats Testing**
- Compared town demographics against ONS/Census 2021 national benchmarks
- Z-tests for unemployment rate and student population
- T-tests for mean age and household size
- All key differences statistically significant (p < 0.001)

**Visualisations**
- Age histogram, gender bar chart, marital status distribution
- Age by marital status (boxplot), marital status by gender, age by gender
- Religion distribution post-cleaning

---

## Key findings

- Population is significantly younger than UK average
- Unemployment notably higher than national rate (statistically significant)
- Student population far exceeds national average — education-focused community
- Household sizes larger than UK norm

---

## Tech stack

```
Python 3 | pandas | matplotlib | seaborn | scipy
```

---

## Files

```
Census_demographic_analysis.ipynb   # main notebook with outputs
README.md
```

The original dataset (T1_A25census-3.csv) is not included — university assessment data.

---

## Why this matters for healthcare AI

Clinical datasets are messy in exactly these ways — missing values, impossible entries, logical inconsistencies. This project is basically a dress rehearsal for what you'd do before training any clinical prediction model. The same imputation decisions (why median not mean for skewed data, why mode for categorical), the same validation logic, the same "does this make sense in the real world" checks — all of that transfers directly.

---

*Part of my MSc AI for Healthcare portfolio — University of Hull, graduating September 2026.*
