# Data Science Muscle Memory: Core Concepts

## 1. Data Cleaning & Preprocessing 
* **Trust but Verify (Diabetes Project):** A dataset might say `0` missing values, but domain knowledge tells you a BMI of `0` is a placeholder for missing data. Always run `df.describe()` to catch these logic errors.
* **The 50% Rule:** If a feature is missing half its data, drop the column. Don't guess. Protect the integrity of the rows you actually have.
* **Median over Mean:** When filling in missing data, the mean gets easily dragged around by extreme outliers (like a massive glucose spike or a billionaire's mansion). Use the median to keep your baseline realistic.

## 2. Exploratory Data Analysis (EDA)
* **Group It to Understand It (Diabetes):** Mixing healthy and unhealthy patients together gives you a useless average. You have to use `groupby()` on your target variable to actually see the mathematical contrast.
* **Visualizing Spread and Outliers (Nigerian Real Estate & Diabetes):** Box plots are the ultimate tool for comparing categories. Whether comparing property prices across different Nigerian neighborhoods or comparing glucose levels between diagnostic groups, `sns.boxplot()` shows you the median, the normal range, and specifically isolates the extreme outliers.
* **Readability Matters (Nigerian Real Estate):** Always format your charts before presenting. Using `plt.figure(figsize=(10, 6))` ensures the data isn't crammed and is actually readable for stakeholders.

## 3. The Golden Rule
* **Context is King:** Never delete an outlier just to clean up a chart. A $10M house in Lagos or a 190 glucose level in a healthy patient might look like an error to a pure coder, but they represent real-world realities. Understand the domain before you alter the data.