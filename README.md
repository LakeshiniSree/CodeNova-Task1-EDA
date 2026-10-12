# Exploratory Data Analysis (EDA) — Breast Cancer Wisconsin Dataset

## 1. Project Overview

This project performs Exploratory Data Analysis (EDA) on the Breast Cancer Wisconsin (Diagnostic) dataset. The objective is to understand the dataset's structure, check data quality, identify potential outliers, and explore relationships between numerical features using statistical analysis and visualizations.

This project is completed as part of the CodeNova AI/ML Internship, Task 1.

## 2. Dataset Information

- **Dataset:** Breast Cancer Wisconsin (Diagnostic)
- **Source:** UCI Machine Learning Repository
- **Dataset link:** https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic
- **Total records:** 569
- **Total columns:** 32
- **Numerical features:** 30
- **Target column:** `diagnosis`
- **Diagnosis labels:** `M` = Malignant, `B` = Benign

The dataset contains numerical measurements derived from breast mass images. The `ID` column identifies records, while `diagnosis` represents the diagnosis category.

## 3. Tools and Libraries

- Python
- Jupyter Notebook
- Pandas
- Matplotlib
- Seaborn

## 4. Steps Performed

### Step 1: Data Loading
- Loaded the dataset into a Pandas DataFrame.
- Assigned column names to the dataset.
- Examined the first few rows.

### Step 2: Dataset Profiling
- Checked the number of rows and columns.
- Examined data types using `df.info()`.
- Generated descriptive statistics using `df.describe()`.

### Step 3: Data Quality Checks
- Checked for missing values.
- Checked for duplicate rows.
- Used the Interquartile Range (IQR) method to identify potential outliers.

### Step 4: Data Visualization
- Diagnosis distribution plot.
- Histograms of selected numerical features.
- Boxplots of selected numerical features.
- Correlation heatmap.
- Pairwise scatter plots of selected features, grouped by diagnosis.

### Step 5: Statistical Analysis
Compared the average values of `radius_mean`, `texture_mean`, `perimeter_mean`, and `area_mean` across the two diagnosis categories.

## 5. Key Findings

- The dataset contains 569 records and 32 columns.
- The data quality checks found no missing values.
- No duplicate rows were detected.
- The IQR method identified 608 potential outlier values across the numerical features.
- Histograms and boxplots were used to investigate feature distributions and potential outliers.
- The correlation heatmap was used to examine relationships among numerical features.
- Pairwise scatter plots were used to explore relationships between selected features and diagnosis categories.

**Note:** Potential outliers were not automatically removed because they may represent genuine measurements.

## 6. Project Structure

```text
Task-1/
├── EDA_Breast_Cancer.ipynb
├── README.md
└── breast+cancer+wisconsin+diagnostic/
    ├── wdbc.data
    └── wdbc.names
```

## 7. How to Run the Project

1. Install Python and Jupyter Notebook.
2. Install the required libraries:

   ```bash
   python -m pip install pandas matplotlib seaborn notebook
   ```

3. Download and extract the dataset from the UCI Machine Learning Repository.
4. Update the dataset folder path in the notebook if necessary.
5. Open the notebook in Jupyter Notebook.
6. Run the cells in order to reproduce the analysis and visualizations.

## 8. Conclusion

This project demonstrates the use of exploratory data analysis to understand a real-world dataset. Data profiling, quality checks, outlier detection, statistical summaries, and visualizations were used to investigate the dataset before any predictive modeling.

The analysis provides a foundation for further feature analysis and machine learning experiments. It does not itself establish a clinical diagnosis or replace professional medical evaluation.

## 9. Author

**CodeNova AI/ML Internship — Task 1: EDA**