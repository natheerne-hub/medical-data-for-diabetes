# 🩸 Diabetes Medical Data Analysis

### Healthcare Data Cleaning & Exploratory Analysis | Dr. Natheer Soliman, MD

A healthcare data analysis project focused on cleaning, exploring, and understanding clinical variables associated with diabetes.

## 🎯 Project Objective

The project demonstrates a practical healthcare data workflow: identify data-quality problems, apply clinically informed preprocessing, explore distributions, and prepare the dataset for further statistical or machine-learning analysis.

## 🔎 Analysis Workflow

### 1. Data Exploration

- Inspect dataset dimensions and data types
- Review missing values
- Examine distributions and descriptive statistics

### 2. Clinically Informed Data Cleaning

Several variables contain zero values that may be physiologically implausible or represent missing measurements, including:

- Glucose
- Blood pressure
- Skin thickness
- Insulin
- BMI

These values were treated as missing (`NaN`) before further analysis.

### 3. Missing-Value Imputation

Missing values were imputed using the **median**, reducing sensitivity to extreme observations.

### 4. Outlier Analysis

Box plots were used to inspect distributions and identify potential extreme observations, particularly in variables such as insulin.

## 🧰 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## 📁 Repository Contents

- `diabetes.csv` — original dataset
- `Untitled0 (1).ipynb` — analysis notebook

## ⚠️ Important Note

This project is for **educational and portfolio purposes**. Data cleaning decisions are context-dependent and should be validated against the clinical meaning, measurement process, and source documentation of a real healthcare dataset.

## 👨‍⚕️ Author

**Dr. Natheer Soliman, MD**  
Healthcare Data Analyst | Clinical Data & AI
