# Cardiovascular Disease Analysis

## Project Overview

This project analyzes cardiovascular disease prevalence using Python and a dataset containing 70,000 patient records before cleaning. After addressing unrealistic measurements and data quality issues, 68,576 observations remained for analysis.

The objective was to investigate how patient characteristics, including age, physical activity, blood pressure, BMI, and cholesterol levels, relate to cardiovascular disease prevalence.

The analysis combines exploratory data analysis, data visualization, and logistic regression to identify patterns, compare patient groups, and evaluate statistical associations.

### Tools and Technologies

- **Python:** Data analysis and statistical modeling
- **Pandas:** Data cleaning, transformation, and aggregation
- **Matplotlib:** Data visualization
- **Statsmodels:** Logistic regression and likelihood ratio testing
- **Jupyter Notebook:** Analysis documentation and reproducible workflow


## Research Questions

This analysis focused on three research questions:

1. **Age and Physical Activity:** How does cardiovascular disease prevalence vary across age groups, and how does physical activity relate to that prevalence?
2. **Blood Pressure:** Does elevated blood pressure correspond to higher cardiovascular disease prevalence, and does that relationship differ by age?
3. **BMI and Cholesterol:** Is BMI or cholesterol more strongly associated with cardiovascular disease after accounting for age?

## Dataset Overview

The analysis uses the Cardiovascular Disease Dataset from Kaggle, containing 70,000 patient records and variables related to cardiovascular health.

The dataset includes:

- **Demographics:** Age and gender.
- **Physical Measurements:** Height, weight, systolic blood pressure, and diastolic blood pressure.
- **Health Indicators:** Cholesterol and glucose levels.
- **Lifestyle Factors:** Smoking status, alcohol consumption, and physical activity.
- **Target Variable:** Cardiovascular disease status (0 = No disease, 1 = Disease).

After data cleaning, 68,576 patients records remained for analysis.

## Data Cleaning and Preparation

The dataset underwent several cleaning and transformation steps before analysis:

1. **Missing Values and Duplicates:** Check for missing values and duplicate records.
2. **Blood Pressure:** Identified and removed unrealistic systolic and diastolic blood pressure measurements.
3. **Height and Weight:** Investigated extreme measurements and removed observations considered implausible.
4. **Age Conversion:** Converted patient age from days into years to improve interpretability.
5. **BMI Calculations:** Calculated Boston Mass Index (BMI) using height and weight, then categorized patients into BMI groups.
6. **Age Groups:** Created age categories to compare cardiovascular disease prevalence across different age ranges.
7. **Blood Pressure Categories:** Classified patients into blood pressure groups for prevalence comparisons.

These steps produced a cleaned dataset suitable for exploratory analysis, visualization, and logistic regression.
