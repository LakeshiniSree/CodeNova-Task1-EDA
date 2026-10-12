# Exploratory Data Analysis (EDA) — Breast Cancer Wisconsin Dataset

## 1. Project Overview

This project performs Exploratory Data Analysis (EDA) on the **Breast Cancer Wisconsin (Diagnostic) Dataset**. The objective is to understand the dataset's structure, examine data quality, identify potential outliers, analyze feature distributions, and explore relationships between numerical features using statistical analysis and visualizations.

This project was completed as part of the **CodeNova AI/ML Internship — Task 1: Exploratory Data Analysis**.

## 2. Dataset Information

- **Dataset Name:** Breast Cancer Wisconsin (Diagnostic)
- **Source:** UCI Machine Learning Repository
- **Dataset Link:** https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
- **Total Records:** 569
- **Total Columns:** 32
- **Numerical Features:** 30
- **Target Column:** `diagnosis`
- **Diagnosis Labels:**
  - `M` — Malignant
  - `B` — Benign

The dataset contains numerical measurements computed from digitized images of breast mass samples. The `ID` column identifies each record, and the `diagnosis` column represents the diagnosis category.

## 3. Tools and Libraries Used

- **Python** — Programming language used for data analysis.
- **Jupyter Notebook** — Environment used to execute code and document the analysis.
- **Pandas** — Data loading, manipulation, and statistical analysis.
- **NumPy** — Numerical computing.
- **Matplotlib** — Plot creation and customization.
- **Seaborn** — Statistical data visualization.

## 4. Steps Performed

### Step 1: Data Loading

- Loaded the dataset into a Pandas DataFrame.
- Assigned descriptive column names using the dataset documentation.
- Displayed the first few rows to inspect the data.
- Verified the dataset dimensions.

### Step 2: Dataset Profiling

- Checked the number of rows and columns using `df.shape`.
- Examined column names, data types, and non-null counts using `df.info()`.
- Generated descriptive statistics using `df.describe()`.
- Reviewed numerical feature ranges and summary statistics.

### Step 3: Missing Values and Duplicate Checks

- Checked missing values using `df.isnull().sum()`.
- Checked duplicate records using `df.duplicated().sum()`.

**Findings:**
- Total missing values: 0.
- Total duplicate rows: 0.

No missing-value imputation or duplicate-row removal was required.

### Step 4: Outlier Detection

- Applied the Interquartile Range (IQR) method to numerical features.
- Calculated the first quartile (Q1), third quartile (Q3), and IQR.
- Identified values below the lower bound or above the upper bound as potential outliers.

The IQR method identified **608 potential outlier values** across the numerical features. These values were retained because statistical outliers may represent genuine measurements. They should not be removed without further investigation.

### Step 5: Diagnosis Distribution

Created a count plot to compare the numbers of benign and malignant cases.

This visualization helps examine the distribution of the target variable and identify whether the diagnosis categories are balanced.

### Step 6: Feature Distribution Analysis

Created histograms for selected numerical features.

The histograms help examine:
- The distribution and spread of feature values.
- Concentrations of observations.
- Skewness and possible unusual values.
- Differences in the distributions of selected measurements.

### Step 7: Boxplot Analysis

Created boxplots for selected numerical features.

Boxplots were used to examine:
- The median and interquartile range.
- Variation in feature values.
- Potential outliers.
- Differences in the spread of numerical measurements.

### Step 8: Correlation Analysis

Created a correlation heatmap for the numerical features.

The heatmap helps identify:
- Strong positive relationships.
- Strong negative relationships.
- Weak linear relationships.
- Groups of features that may contain related information.

Correlation indicates association, not necessarily causation.

### Step 9: Pairwise Scatter Plot Analysis

Created pairwise scatter plots for the following selected features:

- `radius_mean`
- `texture_mean`
- `perimeter_mean`
- `area_mean`

The observations were colored by diagnosis category to explore relationships between features and potential differences between benign and malignant cases.

The plots show strong positive relationships among `radius_mean`, `perimeter_mean`, and `area_mean`. The diagnosis categories also show differences for some feature combinations, although some overlap remains.

### Step 10: Statistical Comparison

Calculated the average values of selected features for each diagnosis category:

- `radius_mean`
- `texture_mean`
- `perimeter_mean`
- `area_mean`

This comparison helps identify differences in the average measurements between benign and malignant cases.

## 5. Key Findings

- The dataset contains **569 records and 32 columns**, including an ID column, a diagnosis column, and 30 numerical features.
- The dataset contains no missing values.
- No duplicate rows were detected.
- The IQR method identified 608 potential outlier values across the numerical features.
- Potential outliers were retained rather than automatically removed.
- Histograms and boxplots helped examine feature distributions and potential outliers.
- The correlation heatmap helped reveal relationships among numerical features.
- `radius_mean`, `perimeter_mean`, and `area_mean` show strong positive relationships.
- Pairwise scatter plots reveal differences between the diagnosis categories for some feature combinations, with some overlap.
- Grouped averages provide an additional way to compare selected measurements across diagnosis categories.

These findings describe patterns in this dataset and do not establish a clinical diagnosis or replace professional medical evaluation.

## 6. Project Structure

```text
Task-1/
├── CodeNova_Task1_EDA.ipynb
├── README.md
├── images/
│   ├── diagnosis_distribution.png
│   ├── feature_histograms.png
│   ├── feature_boxplots.png
│   ├── correlation_heatmap.png
│   └── pairwise_scatterplot.png
└── breast+cancer+wisconsin+diagnostic/
    ├── wdbc.data
    └── wdbc.names
```

The `CodeNova_Task1_EDA.ipynb` file contains the executed analysis and Markdown explanations. The `images/` folder contains exported visualization files, and the dataset folder contains the original data and documentation files.

## 7. How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook.

### Install the Required Libraries

Run the following command in a terminal:

```bash
python -m pip install pandas numpy matplotlib seaborn notebook
```

### Execution Steps

1. Download the Breast Cancer Wisconsin (Diagnostic) dataset from the UCI Machine Learning Repository.
2. Extract the dataset files into the project directory.
3. Open `CodeNova_Task1_EDA.ipynb` in Jupyter Notebook or JupyterLab.
4. Check that the dataset path in the notebook matches your local folder.
5. Execute the notebook cells in order.
6. Review the generated tables, plots, and Markdown observations.
7. Save the notebook after execution.

## 8. Conclusion

This project demonstrates how Exploratory Data Analysis can be used to understand a real-world dataset before applying machine learning algorithms.

The analysis included dataset profiling, missing-value and duplicate checks, IQR-based outlier detection, descriptive statistics, feature distributions, boxplots, correlation analysis, pairwise scatter plots, and grouped feature comparisons.

The results provide an initial understanding of the dataset's quality, feature relationships, and diagnosis-related patterns. This analysis can serve as a foundation for further feature analysis and machine learning experiments.

## 9. Deliverables

- Executed Jupyter Notebook with code, outputs, and Markdown commentary.
- Exported visualization images.
- README documentation describing the dataset, methodology, and key findings.

## 10. Author and Internship Details

**Program:** CodeNova AI/ML Internship  
**Task:** Task 1 — Exploratory Data Analysis  
**Project:** Breast Cancer Wisconsin Dataset EDA
