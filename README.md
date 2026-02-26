# Census Demographic Analysis

MSc AI for Healthcare | University of Hull | Fundamentals of Data Science

## What this is

Took a messy UK census dataset and cleaned it, analysed it, and compared it against national averages. The whole point was figuring out what makes this population different from the rest of the UK, and whether those differences are actually significant or just noise.

Real-world data is dirty. This project is about fixing that before you do anything useful with it.

## What I built

Started with missing values everywhere. Age had gaps so I used median imputation (not mean, because the distribution was skewed). Religion was categorical so mode made more sense there. Also caught things like negative ages, people listed as married under 18, kids assigned to adult occupation categories. Fixed or flagged each one with a reason.

Once the data was clean, ran the actual analysis. Age distribution, gender split, household sizes, occupation breakdown. Found the student population was way higher than expected, so dug into that.

Then compared everything against ONS national benchmarks. Used Z-tests for proportions (unemployment rate, student population) and T-tests for continuous variables (mean age, household size). Everything came back significant at p < 0.001.

## What I found

The town skews young. Unemployment is higher than the national rate. Student population is way above average. Households are bigger than the UK norm. Taken together it looks like a university town, which the occupation data backs up.

## What I learned

Median imputation for skewed continuous data, mode for categorical. How to catch logical inconsistencies in a dataset, not just missing values. How to run and interpret Z-tests vs T-tests depending on what you're comparing. And honestly, how much time data cleaning actually takes compared to the analysis itself.

The tricky part was the age validation. Just checking for nulls wasn't enough. Had to think about what ages are actually possible and what combinations of fields make no sense together.

## Tech

Python, pandas, matplotlib, seaborn, scipy

## Files

Census_demographic_analysis.ipynb has everything including outputs.

Dataset not included, it's university assessment data.

## Why it matters for healthcare AI

Clinical data looks exactly like this. Missing values, impossible entries, fields that contradict each other. Everything I did here is what you'd do before training any kind of clinical prediction model. Get the data right first or the model is useless.

University of Hull, MSc AI for Healthcare, graduating September 2026.
