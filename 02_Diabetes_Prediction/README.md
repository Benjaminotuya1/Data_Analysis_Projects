# Clinical Diabetes Data: Exploratory Data Analysis

## Overview
This project focuses on cleaning and analyzing a raw clinical dataset to extract physiological insights about diabetes. The main objective was to handle hidden data entry errors and visually prove the statistical difference between healthy and diabetic patient markers.

## Tools
* Python (Pandas for data manipulation)
* Seaborn & Matplotlib (for visualization)

## The Process
1. **Exposing Hidden Nulls:** Identified that missing patient vitals were falsely recorded as `0` and converted them to standard `NaN` values to prevent skewed math.
2. **Data Imputation & Dropping:** Dropped the `Insulin` column entirely due to a 50% null rate. Imputed minor missing values in `Glucose`, `BloodPressure`, and `BMI` using the median to maintain clinical accuracy.
3. **EDA & Visualization:** Grouped patients by diagnosis and used box plots to compare metrics. Successfully visualized the stark contrast in median glucose levels (110 vs. 142) and identified valid physiological outliers, like postprandial glucose spikes in non-diabetic patients.