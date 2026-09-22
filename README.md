# Heart Disease Patient Data Analysis

An R-based statistical analysis and visualization project on the Heart Disease UCI dataset, built with R Markdown. The project covers data importing, cleaning, exploratory analysis, and visualization to uncover clinical patterns related to heart disease diagnosis.

## Overview

Heart disease is one of the leading causes of death worldwide, and identifying patterns in patient health data can help with early detection and prevention. This project analyzes the **Heart Disease dataset** (originally from the UCI Machine Learning Repository, widely available on Kaggle as "Heart Disease UCI") using R.

The analysis covers chest pain types, thalassemia test results, cholesterol levels, and the relationship between age and maximum heart rate, with the goal of surfacing meaningful, data-driven health insights.

## Objectives

- Import and understand the heart disease dataset using R
- Clean and preprocess the dataset before analysis
- Check for missing values and data inconsistencies
- Identify the most common chest pain types among patients
- Analyze the distribution of thalassemia test results
- Study cholesterol level distribution across patients
- Examine the relationship between age and maximum heart rate
- Create meaningful graphs and visualizations using R
- Interpret the results and identify important clinical insights

## Dataset

| | |
|---|---|
| **File** | `heart_disease_dataset.csv` |
| **Source** | UCI Machine Learning Repository / Kaggle ("Heart Disease UCI") |
| **Observations** | 247 patients |
| **Variables** | 14 |
| **Missing values** | None |

**Variables:**

| Column | Description |
|---|---|
| `age` | Age of the patient |
| `sex` | Sex (1 = male, 0 = female) |
| `cp` | Chest pain type (1–4) |
| `trestbps` | Resting blood pressure (mm Hg) |
| `chol` | Serum cholesterol (mg/dl) |
| `fbs` | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) |
| `restecg` | Resting ECG results |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina (1 = yes, 0 = no) |
| `oldpeak` | ST depression induced by exercise |
| `slope` | Slope of the peak exercise ST segment |
| `ca` | Number of major vessels colored by fluoroscopy |
| `thal` | Thalassemia test result (fixed, normal, reversible) |
| `target` | Heart disease diagnosis (1 = present, 0 = absent) |

## Project Structure

```
.
├── Heart_Disease_Analysis.Rmd    # R Markdown source (analysis + narrative)
├── Heart_Disease_Analysis.html   # Rendered HTML report
├── Heart_Disease_Analysis_with_cover.pdf  # Rendered PDF report with cover page
├── heart_disease_dataset.csv     # Source dataset
└── README.md
```

## Requirements

- [R](https://www.r-project.org/) (≥ 4.0)
- [RStudio](https://posit.co/download/rstudio-desktop/) (recommended)
- R packages: `rmarkdown`, `knitr` (base R plotting functions are used for charts, so no additional visualization packages are required)

Install the required packages if needed:

```r
install.packages(c("rmarkdown", "knitr"))
```

## How to Run

1. Clone or download this repository.
2. Open `Heart_Disease_Analysis.Rmd` in RStudio, making sure `heart_disease_dataset.csv` is in the same working directory.
3. Click **Knit** (or run in R):

```r
rmarkdown::render("Heart_Disease_Analysis.Rmd")
```

This regenerates the HTML report. The PDF version with the cover page is a separately packaged deliverable.

## Analysis Workflow

1. **Data Importing** — Load the dataset with `read.csv()` and preview it with `head()`
2. **Understanding the Dataset** — Inspect structure (`str()`) and summary statistics (`summary()`)
3. **Missing Value Check** — Verify data completeness with `colSums(is.na(...))`
4. **Data Cleaning** — Convert numeric codes (`cp`, `sex`, `target`) into readable factor labels
5. **Cholesterol Analysis** — Mean, median, variance, and standard deviation of cholesterol levels
6. **Chest Pain Type Analysis** — Frequency table and bar chart
7. **Thalassemia Analysis** — Frequency table and bar chart
8. **Diagnosis Analysis** — Pie chart of disease presence vs. absence
9. **Cholesterol Distribution** — Histogram
10. **Age vs. Maximum Heart Rate** — Scatter plot and Pearson correlation

## Key Findings

- The dataset contains 247 patient records with no missing values across any of the 14 variables.
- **Asymptomatic** chest pain is the most common type (116 patients), followed by non-anginal pain (68), atypical angina (44), and typical angina (19).
- A **normal** thalassemia test result is the most common outcome (142 patients), followed by reversible (88) and fixed (17) defects.
- 66 of 247 patients (26.7%) are diagnosed with heart disease; 181 (73.3%) are not.
- Cholesterol levels are right-skewed: mean ≈ 247.4 mg/dl, median = 243.0 mg/dl, with a few unusually high values.
- Age and maximum heart rate show a **moderate negative correlation** (r ≈ -0.41) — older patients tend to achieve a lower maximum heart rate.

## Conclusion

This project demonstrates how R can be used to explore, clean, and visualize real-world health data, turning raw clinical records into interpretable statistical insights. The workflow — import, clean, analyze, visualize, interpret — mirrors a standard exploratory data analysis pipeline applicable to other health or tabular datasets.

## References

- [Heart Disease Dataset — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/45/heart+disease)
- [R Programming Documentation](https://www.r-project.org/other-docs.html)
- [R Markdown Documentation](https://rmarkdown.rstudio.com/)

## Author

**Pranay Upadhyay**
BSc IT (Regular), Division E
Parul University — R Programming coursework
