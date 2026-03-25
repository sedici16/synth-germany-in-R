# Synthetic Control Method — Germany

An econometric analysis using the Synthetic Control Method (SCM) to estimate the causal effect of a policy intervention on Germany's economy. Built in R using the `Synth` package.

## What It Does

Constructs a "synthetic Germany" from a weighted combination of other European countries to serve as a counterfactual — what would Germany's economic indicators have looked like without the intervention?

## Methodology

1. **Data Collection** — Economic indicators (inflation, imports, public debt, deficit, expenditure) across European countries from an Excel dataset
2. **Data Cleaning** — Removes countries with excessive missing data (Estonia, Slovenia, Latvia, Lithuania, Luxembourg, Belgium), interpolates remaining gaps
3. **Synthetic Control** — Uses the `Synth` package to find optimal country weights that best approximate pre-treatment Germany
4. **Analysis** — Compares actual Germany vs synthetic Germany post-treatment to estimate the causal effect

## Key Findings

- Predictor weights show inflation and public debt are the most influential variables in constructing the synthetic control
- Country weights reveal which European economies best approximate Germany's pre-treatment trajectory

## Tech Stack

- **Language**: R
- **Packages**: tidyverse, readxl, Synth
- **Data**: GER_clean.xlsx (multi-sheet Excel with economic indicators)

## Files

```
├── synth_final_3.Rmd      # Full analysis (data cleaning + SCM)
├── synth_final_3.nb.html  # Rendered notebook with results
└── GER_clean.xlsx         # Source data
```

## Running

Open `synth_final_3.Rmd` in RStudio and knit, or run chunks interactively.

```r
install.packages(c("tidyverse", "readxl", "Synth"))
```
