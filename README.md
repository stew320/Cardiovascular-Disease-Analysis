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
5. **BMI Calculations:** Calculated Body Mass Index (BMI) using height and weight, then categorized patients into BMI groups.
6. **Age Groups:** Created age categories to compare cardiovascular disease prevalence across different age ranges.
7. **Blood Pressure Categories:** Classified patients into blood pressure groups for prevalence comparisons.

These steps produced a cleaned dataset suitable for exploratory analysis, visualization, and logistic regression.

## Analysis and Key Findings

### Question 1: Age and Physical Activity

**Research Question:** How does cardiovascular disease prevalence vary across age groups, and how does physical activity relate to that prevalence?

**Key Findings:**

- Cardiovascular disease prevalence generally increased across older age groups.
- Within each age group analyzed, physically active patients demonstrated lower cardiovascular disease prevalence than inactive patients.
- Among patients aged 55-59, prevalence was 60.1% for inactive patients compared with 55.1% for active patients, a difference of 5 percentage points.
- The 25-34 age group contained only four observations and was excluded from the age/activity visualization due to its extremely small sample size.

**Interpretation**

The findings suggest that age is positively associated with cardiovascular disease prevalence, while physical activity is associated with lower prevalence within the age group examined. These relationships are observational and do not establish causation.

### Question 2: Blood Pressure

**Research Question:** Does elevated blood pressure correspond to higher cardiovascular disease prevalence, and does that relationship differ by age?

**Key Findings:**

- Normal blood pressure: 22.1% cardiovascular disease prevalence.
- Elevated blood pressure: 32.3% prevalence.
- Stage 1 hypertension: 38.5% prevalence.
- Stage 2 hypertension: 78.0% prevalence.

**Interpreation**

Cardiovascular disease prevalence increased across higher blood pressure categories. Patients classified as Stage 2 hypertension demonstrated substantially higher prevalence than patients with Normal blood pressure.

These findings indicate a strong association between elevated blood pressure and cardiovascular disease status within the dataset.

### Question 3: BMI and Cholesterol

**Research Question:** Is BMI or cholesterol more strongly associated with cardiovascular disease after accounting for age?

**Key Findings:**

- Cardiovascular disease prevalence increased from 27.5% among Underweight patients to 62.4% among Obese patients.
- Prevalence increased from 43.5% among patients with Normal cholesterol to 76.2% among patients with Well Above Normal cholesterol.
- Logistic regression showed that both BMI category and cholesterol level were statistically significant predictors after accounting for age and the other included variable (p < 0.001).
- Removing BMI from the full model produced a likelihood ratio statistic of approximately 1,323.37.
- Removing cholesterol produced a larger likelihood ratio statistic of approximately 2,060.64.

**Interpretation**

Both BMI and cholesterol were associated with cardiovascular disease after adjusting for age and the other included predictor.

Removing cholesterol caused a greater deterioration in model fit than removing BMI, suggesting that cholesterol contributed more incremental explanatory information within this model specification.

These results do not establish that cholesterol is universally a stronger predictor than BMI.

## Statistical Modeling

A logistic regression model was developed using Statsmodels to examine the relationship between age, BMI category, cholesterol level, and cardiovascular disease status.

### Model Results

- **Observations:** 68,576
- **Dependent Variable:** Cardiovascular disease status (0 = No disease, 1 = Disease)
- **Independent Variables:** Age, BMI category, cholesterol level
- **McFadden Pseudo R-squared:** 0.0835
- **Statistical Significance:** All included predictor coefficients were statistically significant (p < 0.001).

### Adjusted Odds Ratios

The logistic regression produced the following results:

- **Age:** Each additional year was associated with approximately 6.7% higher odds of cardiovascular disease.
- **Obese:** Patients classified as Obese had approximately 3.42 times the odds of cardiovascular disease compared with Underweight patients.
- **Well Above Normal Cholesterol:** Patients with Level 3 cholesterol had approximately 3.16 times the odds of cardiovascular disease compared with patients with Normal cholesterol.

These comparisons account for the other predictors included in the model. Odds ratios describe differences in odds, not direct changes in probability.

## Project Limitations

Several limitations should be considered when interpreting the findings:

1. **Observational Data:** The analysis identifies statistical associations but cannot establish causation.
2. **Uneven Sample Sizes:** Some patient groups contained substantially fewer observations, including the Underweight BMI category and the youngest age group.
3. **Data Cleaning:** Removing implausible measurements may have introduced selection bias or affected the distribution of the analyzed population.
4. **Limited Predictors:** The logistic regression included age, BMI, cholesterol but excluded other potentially relevant factors such as smoking, physical activity, and blood pressure.
5. **Model Validation:** The logistic regression was not evaluated using a separate test dataset, so its performance on unseen observations has not been established.

### Future Improvements

Future analysis could include:

- Expanding the regression model to incorporate additional patient characteristics.
- Evaluating predictive performance using a train/test split and metrics such as precision, recall, and ROC-AUC.
- Investigating interactions between variables to determine whether associations differ across patient groups.

## Full Python Analysis

The complete analysis, including data cleaning, exploratory data analysis, visualizations, logistic regression, and statistical interpretations, is available in the Jupyter notebook.

**View the complete project:**

[Cardiovascular Disease Analysis - Jupyter Notebook](cardio_vasc.ipynb)
