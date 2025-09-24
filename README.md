This repository contains a statistical analysis project. 
The project demonstrates data import, cleaning, exploratory data analysis, hypothesis testing, various regression techniques, and random forest modeling using R. 
The scripts are written in R Markdown, making it easy to generate reports in PDF or Word format.

## Project Overview

- **Author:** Asmatahasin  
- **Date:** 2023-05-01  
- **Description:**  
  The project focuses on a comprehensive data analysis workflow using a dataset imported from a CSV file. Key steps include:
  - Importing and previewing the dataset.
  - Selecting and cleaning data by handling missing values and outliers.
  - Conducting exploratory data analysis (EDA) with summary statistics, boxplots, histograms, and correlation plots.
  - Performing a range of statistical tests (t-test, Wilcoxon rank-sum, Kruskal-Wallis, Mann-Whitney U test).
  - Building regression models (multiple linear regression and logistic regression).
  - Implementing and tuning a random forest model for classification.

## Repository Structure

## Key Sections in the Analysis

### 1. Data Import and Preprocessing
- **Importing the Dataset:**  
  The CSV file is loaded into R, and initial data exploration (e.g., `head()`, `str()`, `summary()`) is performed.
- **Selecting Columns:**  
  Specific columns (e.g., Age, Gender, BMI, Ca, P, Mg, OP, Smoking, Drinking) are selected for further analysis.
- **Missing Values:**  
  The script checks for null values and replaces them with the mean of the corresponding columns.

### 2. Outlier Detection and Cleaning
- **Boxplot Visualization:**  
  Boxplots are used to detect outliers.
- **Outlier Replacement:**  
  Outliers in the dataset are replaced with the median value using a custom function.

### 3. Exploratory Data Analysis (EDA)
- **Descriptive Statistics:**  
  Summary statistics and data structure are reviewed.
- **Visualization:**  
  Histograms and correlation plots (using `corrplot`) provide visual insights into the data distributions and relationships.
- **Q-Q Plots:**  
  Normality of specific variables (e.g., `OP`) is assessed via Q-Q plots.

### 4. Statistical Tests
- **One-Sample t-Test:**  
  Tests whether the mean of each column significantly differs from zero.
- **Paired t-Tests:**  
  Comparisons between variables, including a specific focus on `OP`.
- **Non-parametric Tests:**  
  Wilcoxon rank-sum, Kruskal-Wallis, and Mann-Whitney U tests are applied to explore group differences based on gender and age groups.

### 5. Regression Modeling
- **Multiple Linear Regression:**  
  Several regression models are built to predict the `OP` variable using different sets of predictors (e.g., BMI, Smoking, Drinking; Ca, Mg, P; Age, Gender).
- **Logistic Regression:**  
  Logistic regression models are fitted to classify `OP` based on various predictor combinations.

### 6. Random Forest Modeling
- **Model Building:**  
  A random forest classifier is trained, and its performance is evaluated via a confusion matrix.
- **Hyperparameter Tuning:**  
  The model’s hyperparameters (`ntree` and `mtry`) are tuned using grid search and cross-validation, with performance metrics such as accuracy, sensitivity, and specificity evaluated.

## Requirements

To run the analysis, ensure you have the following R packages installed:
- `dplyr`
- `corrplot`
- `randomForest`
- `caret`

You can install these packages using:

```r
install.packages(c("dplyr", "corrplot", "randomForest", "caret"))
```
##How to Run:
1. Clone the Repository:  
```r
git clone https://github.com/asmatahasin/stats-projects.git
```
2. Place the Dataset:
Download and Ensure that `UA.csv` is located in the designated folder or update the path accordingly in the R script).
3. Open the R Markdown file:
Open `AA Project.Rmd` 
4. Knit the document:
Use RStudio's "Knit" button to generate a PDF or Word report.

##License
This Project is licensed under the MIT License.
