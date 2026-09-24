<p align="center"><img src="assets/diabetes-banner.svg" alt="Diabetes Medical Data Analysis" width="100%"></p>

# 🩸 Diabetes Medical Data Analysis

[![Verify Diabetes Notebook](https://github.com/natheerne-hub/medical-data-for-diabetes/actions/workflows/notebook-ci.yml/badge.svg)](https://github.com/natheerne-hub/medical-data-for-diabetes/actions/workflows/notebook-ci.yml)

### Healthcare Data Cleaning, EDA & Statistical Analysis | Dr. Nather Yunis Suliaman, MD

A reproducible healthcare analytics project focused on **clinical data quality, exploratory analysis, statistical comparison, and cautious interpretation** of diabetes-related variables.

## Project objective

Demonstrate a practical analytical workflow in which data quality is treated as part of the clinical problem: inspect the raw structure, identify implausible zero-coded physiological measurements, document preprocessing decisions, explore outcome patterns, quantify group differences, and avoid causal or diagnostic overinterpretation.

## Dataset snapshot

- **768 observations**
- **9 variables**
- Variables include glucose, blood pressure, BMI, insulin, age, pregnancies, diabetes pedigree function and a binary diabetes outcome.

### Provenance guardrail

The repository copy has the structure commonly associated with the 768-row Pima diabetes dataset, but the **exact upstream source, citation and redistribution license cannot be verified from the repository history currently available**.

For that reason:

- the repository does not claim a more specific provenance than can be supported;
- the CSV should not be republished as a new dataset on external platforms without verified redistribution rights;
- analytical conclusions are framed as findings from the repository dataset rather than claims about a broader population.

This is an intentional data-governance decision. In healthcare analytics, uncertain provenance should be made visible rather than filled with an assumed citation.

## Analysis workflow

1. Inspect shape, data types, descriptive statistics and missingness.
2. Treat selected zero-coded physiological measurements in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin` and `BMI` as likely missing/unrecorded values for the exploratory workflow.
3. Apply median imputation while preserving the original source data separately in the notebook.
4. Review potential extreme observations with box plots and IQR diagnostics without automatically deleting clinically plausible values.
5. Explore outcome distribution, feature distributions, correlations and relationships with diabetes status.
6. Compare outcome groups using Welch's independent-samples t-tests.
7. Report effect sizes and apply Benjamini–Hochberg FDR correction across feature tests.

## Analytical principles demonstrated

- Clinical plausibility matters when interpreting apparent numeric values.
- Missing-data decisions are documented rather than silently applied.
- Outliers are reviewed before modification.
- Statistical significance is considered alongside effect size.
- Multiple comparisons are explicitly addressed.
- Association is not presented as causation.

## Reproducibility

A GitHub Actions workflow installs the project dependencies and executes the notebook from a clean environment. This provides an automated check for broken paths, missing imports and execution-order problems.

## Repository contents

- [`diabetes_analysis.ipynb`](./diabetes_analysis.ipynb) — complete analysis notebook
- [`diabetes.csv`](./diabetes.csv) — repository dataset; see provenance guardrail above
- [`requirements.txt`](./requirements.txt) — Python dependencies
- [`.github/workflows/notebook-ci.yml`](./.github/workflows/notebook-ci.yml) — automated notebook verification
- [`assets/`](./assets) — visual assets

## Tech stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `SciPy` · `Jupyter / Google Colab` · `GitHub Actions`

## Limitations

- Exact upstream dataset provenance and redistribution rights remain unverified from the available repository history.
- The analysis is observational and cannot establish causality.
- Median imputation does not model uncertainty in missing measurements.
- Statistical significance does not automatically imply clinical significance.
- Predictive modeling would require leakage-safe preprocessing, validation, calibration and appropriate clinical governance.
- This project is a portfolio analysis and not a diagnostic system.

## Author

**Dr. Nather Yunis Suliaman, MD**  
Healthcare Data Analytics · Clinical Analytics · Health Data Quality

[GitHub Profile](https://github.com/natheerne-hub)
