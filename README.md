# 🩸 Diabetes Medical Data Analysis

### Healthcare Data Cleaning, EDA & Statistical Analysis | Dr. Natheer Soliman, MD

A healthcare data analysis project focused on cleaning, exploring, and interpreting clinical variables associated with diabetes.

## 🎯 Project Objective

Demonstrate a practical healthcare analytics workflow: identify data-quality issues, apply clinically informed preprocessing, explore patterns, test group differences, and communicate findings with appropriate clinical caution.

## 📊 Dataset

The dataset contains **768 observations and 9 variables**, including glucose, blood pressure, BMI, insulin, age, pregnancies, diabetes pedigree function, and the binary diabetes outcome.

## 🔎 Analysis Workflow

1. **Data understanding** — inspect shape, data types, descriptive statistics, and missingness.
2. **Clinically informed cleaning** — treat implausible zero values in `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` as missing measurements.
3. **Median imputation** — replace those missing values using column medians to reduce sensitivity to skewed distributions and extreme values.
4. **Exploratory data analysis** — examine outcome distribution, feature distributions, correlations, and relationships with diabetes status.
5. **Outlier review** — inspect potential extreme observations using box plots and IQR-based diagnostics.
6. **Statistical testing** — compare numerical features between outcome groups using independent-samples t-tests with variance checks.

## 🔬 Key Findings

- `Glucose` showed the strongest linear association with diabetes outcome in the exploratory correlation analysis.
- BMI, age, pregnancies, diabetes pedigree function, and insulin also differed between outcome groups in the notebook's statistical comparisons.
- Blood pressure did not show a statistically significant mean difference at the 0.05 threshold in the current analysis.
- The analysis is exploratory: association does not imply causation, and p-values should be interpreted alongside effect size, clinical context, and multiple-testing considerations.

## 🩺 Clinical Interpretation

The project highlights how data-quality decisions can materially affect healthcare analysis. Values such as zero glucose or zero BMI are not treated as valid physiological measurements in this workflow; they are handled as likely missing observations before analysis.

The findings are intended to demonstrate healthcare analytics skills, not to provide diagnosis or individual clinical risk assessment.

## 🧰 Tech Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `SciPy` · `Jupyter / Google Colab`

## 📁 Repository Contents

- [`diabetes_analysis.ipynb`](./diabetes_analysis.ipynb) — complete analysis notebook
- [`diabetes.csv`](./diabetes.csv) — source dataset

## ⚠️ Limitations

- The notebook uses an observational dataset and cannot establish causality.
- Statistical significance does not necessarily imply clinical significance.
- Multiple hypothesis tests should ideally be followed by a correction procedure such as Benjamini–Hochberg FDR.
- Outlier treatment should be justified using source documentation and clinical context before use in real-world analyses.

## 👨‍⚕️ Author

**Dr. Natheer Soliman, MD**  
Healthcare Data Analyst | Clinical Data & AI
