# Adult-Census-Income-Dataset

<img width="765" height="401" alt="Image" src="https://github.com/user-attachments/assets/91147182-e29f-47a4-9a99-1183ac715d7d" />

## Introduction
This dataset contains information about individuals from the 1994 US Census, with the goal of predicting whether a person's income exceeds $50,000 per year. The dataset includes demographic and employment information, such as age, education level, occupation, and work hours per week. The dataset contains 48,842 instances, but 32,562 of the data was use in the course of this study, with a mix of continuous and categorical variables. The data is mostly complete, with some missing values in the native-country feature. The income variable is imbalanced, with approximately 76% of instances having an income of <=50K and 24% having an income of >50K.
## Potential Use Questions:
•	Predicting individual income levels based on demographic and employment information (such as sex, educational level, marital status, occupation, race, country and age).
•	Does work hours determines individuals income?
•	Analyzing the relationships between hours-per-week, capital-gain and capital-loss on income.
# Income Classification and Demographic Analysis Project

---

## Dataset Features

- **Age**: Continuous variable representing the individual's age.
- **Workclass**: Categorical variable representing the individual's work class (e.g., Private, Self-emp-not-inc, Government).
- **Fnlwgt**: Continuous variable representing the individual's final weight.
- **Education**: Categorical variable representing the highest education level attained (e.g., HS-grad, Some-college).
- **Sex**: Categorical variable indicating gender (Male, Female).
- **Country**: Categorical variable representing the country of residence.
- **Income2**: Binary indicator for income level (0 = below threshold, 1 = above threshold).
- Additional features as per dataset.

---

# 📊 Income Prediction Analysis

This project explores how different features influence **predicted income levels** using a binary classification of income (`New Income2`):  
- `0` = Income ≤ 50K  
- `1` = Income > 50K

The analysis includes interpretation of **pivot tables** by demographic and work-related categories such as **sex**, **education**, **marital status**, **occupation**, **workclass**, **race**, **age**, and **work hours**.

---

## 📁 Data Overview

- `New Income2`: Target variable (0 = ≤50K, 1 = >50K)
- Dataset contains categorical and numerical features used to predict income

---

## 🔍 Analysis by Feature


### 1. 📌 Sex vs Income

```plaintext
| Sex    | ≤50K | >50K | Total |
|--------|------|------|-------|
| Female | 38.8%|15.04%|33.08% |
| Male   |61.20%|84.96%|66.92% |
✅ Insight: Males are more likely to be predicted to earn above 50K. Females are overrepresented in the lower-income group.

2. 🎓 Education vs Income
plaintext
Copy
Edit
| Education     | ≤50K | >50K | Total |
|---------------|------|------|-------|
| Bachelors     |12.68%|28.33%|16.45% |
| Masters       | 3.09%|12.23%| 5.29% |
| HS-grad       |35.70%|21.36%|32.25% |
| Some-college  |23.88%|17.69%|22.39% |
| < High School |~16.0%| ~3.1%|~13.1% |
✅ Insight: Higher education strongly correlates with higher predicted income. Bachelor's and above significantly boost chances of being in >50K group.

3. 💍 Marital Status vs Income
plaintext
Copy
Edit
| Marital Status    | ≤50K | >50K | Total |
|-------------------|------|------|-------|
| Married-civ-spouse|33.51%|85.35%|45.99% |
| Never-married     |41.23%| 6.26%|32.81% |
| Divorced          |16.10%| 5.90%|13.65% |
✅ Insight: Married individuals are strongly associated with higher income, while never-married and divorced are skewed toward lower income.

4. 🛠️ Occupation vs Income
plaintext
Copy
Edit
| Occupation       | ≤50K | >50K | Total |
|------------------|------|------|-------|
| Exec-managerial  | 8.49%|25.10%|12.49% |
| Prof-specialty   | 9.23%|23.71%|12.71% |
| Adm-clerical     |13.20%| 6.47%|11.58% |
| Other-service    |12.78%| 1.75%|10.12% |
✅ Insight: Executive and professional roles correlate with high income. Service and clerical jobs lean toward lower income.

5. 🏛️ Workclass vs Income
plaintext
Copy
Edit
| Workclass        | ≤50K | >50K | Total |
|------------------|------|------|-------|
| Private          |71.74%|63.30%|69.70% |
| Self-emp-inc     | 2.00%| 7.93%| 3.43% |
| Federal-gov      | 2.38%| 4.73%| 2.95% |
✅ Insight: Self-employed (incorporated) and government workers are more likely to be high earners. Private sector dominates but includes both income levels.

6. 🌍 Race vs Income
plaintext
Copy
Edit
| Race               | ≤50K | >50K | Total |
|--------------------|------|------|-------|
| White              |83.73%|90.77%|85.43% |
| Black              |11.07%| 4.94%| 9.59% |
| Amer-Indian-Eskimo | 1.11%| 0.46%| 0.96% |
✅ Insight: White individuals are overrepresented in the high-income group; other races, especially Black and Indigenous, are more often in the lower-income group.

7. 📅 Age vs Income
plaintext
Copy
Edit
| Age Range | ≤50K | >50K | Total |
|-----------|------|------|-------|
| 17–21     |12.64%| 0.06%| 9.61% |
| 37–41     |10.94%|17.84%|12.60% |
| 42–46     | 9.47%|17.91%|11.50% |
✅ Insight: High-income predictions increase with age, peaking in mid-to-late 40s. Very young adults (<30) are mostly predicted to earn ≤50K.

8. ⏱️ Work Hours vs Income
plaintext
Copy
Edit
| Work Hours | ≤50K | >50K | Total |
|------------|------|------|-------|
| 1–30       |19.78%| 4.51%|16.11% |
| 31–40      |57.05%|46.32%|54.47% |
| 41–60      |20.31%|44.03%|25.96% |
✅ Insight: Individuals working longer hours (41–60+) are much more likely to be predicted to earn above 50K. Part-time hours correlate with lower income.

📌 Conclusion
Education, occupation, work hours, and marital status are the most significant predictors of income.

Race, age, and workclass reveal underlying disparities and societal patterns.

The model reflects real-world economic trends — but also may carry bias based on historical data.

📈 Optional: Visualizations
Consider adding:

Heatmaps of income distribution by age and education

Stacked bar charts for sex, race, and marital status

Line plots for work hours and age vs income probability

🚀 Next Steps
Conduct multivariate regression or classification

Apply model fairness checks (e.g., disparate impact analysis)

Improve model with better feature engineering or bias mitigation

vbnet
Copy
Edit


## Regression Model Summary

| Statistic          | Value          |
|--------------------|----------------|
| Multiple R         | 0.3412         |
| R Square           | 0.1164 (11.6%) |
| Adjusted R Square  | 0.1163         |
| Standard Error     | 0.4019         |
| Observations       | 32,561         |

### ANOVA Table

| Source      | df    | SS         | MS         | F          | Significance F |
|-------------|-------|------------|------------|------------|---------------|
| Regression  | 3     | 693.0663   | 231.0221   | 1429.9905  | 0             |
| Residual    | 32557 | 5252.2596  | 0.1614     |            |               |
| Total       | 32560 | 5945.3259  |            |            |               |

### Interpretation

- The model explains about **11.6%** of variance in income levels.
- The F-statistic is highly significant (p < 0.0001), indicating the regression model fits better than a model with no predictors.
- However, R Square suggests that other variables might also influence income.

---

## Data Visualization

- **Pivot Charts**: Used to analyze income by sex, education, and workclass.  
- **Map Charts**: Considered to visualize geographic distribution of income levels across countries.
- Bar charts and distribution plots illustrate income patterns by demographic categories.

---

## Analysis Notes

- Income distribution shows variation by sex, education, and country.
- The binary income indicator `Income2` allows for classification-based analysis.
- Feature encoding and data preprocessing steps are essential for accurate modeling.
- Categorical variables are encoded appropriately (e.g., one-hot or label encoding) before regression.

---

## Usage Instructions

1. **Load Data**: Import dataset with all features listed.
2. **Preprocess**: Handle missing values, encode categorical variables.
3. **Modeling**: Run linear regression with key predictors (Age, Sex, Education, Workclass).
4. **Evaluate**: Review regression statistics, ANOVA table, and R Square.
5. **Visualize**: Generate pivot charts and map charts for exploratory analysis.
6. **Interpret**: Draw conclusions on how demographic features relate to income.

---

## Future Work

- Explore additional predictors for improving R Square.
- Perform classification modeling for income category prediction.
- Incorporate interaction terms to capture feature relationships.
- Extend geographic visualization with more granular data.

---


## 🌍 Income Distribution by Country (Pivot Table)

| Country               | ≤50K (%) | >50K (%) | Total (%) |
|------------------------|----------|----------|-----------|
| ?                      | 1.77%    | 1.86%    | 1.79%     |
| Cambodia               | 0.05%    | 0.09%    | 0.06%     |
| Canada                 | 0.33%    | 0.50%    | 0.37%     |
| China                  | 0.22%    | 0.04%    | 0.20%     |
| Colombia               | 0.15%    | 0.03%    | 0.13%     |
| Cuba                   | 0.10%    | 0.06%    | 0.09%     |
| Dominican-Republic     | 0.10%    | 0.02%    | 0.09%     |
| Ecuador                | 0.06%    | 0.01%    | 0.05%     |
| El-Salvador            | 0.20%    | 0.03%    | 0.18%     |
| England                | 0.14%    | 0.17%    | 0.15%     |
| France                 | 0.04%    | 0.06%    | 0.05%     |
| Germany                | 0.15%    | 0.26%    | 0.17%     |
| Guatemala              | 0.08%    | 0.01%    | 0.07%     |
| Haiti                  | 0.08%    | 0.01%    | 0.07%     |
| Honduras               | 0.03%    | 0.00%    | 0.03%     |
| Hong                   | 0.03%    | 0.01%    | 0.03%     |
| Hungary                | 0.01%    | 0.01%    | 0.01%     |
| India                  | 0.13%    | 0.34%    | 0.17%     |
| Iran                   | 0.03%    | 0.08%    | 0.04%     |
| Ireland                | 0.05%    | 0.07%    | 0.05%     |
| Italy                  | 0.05%    | 0.08%    | 0.05%     |
| Jamaica                | 0.10%    | 0.04%    | 0.09%     |
| Japan                  | 0.08%    | 0.13%    | 0.09%     |
| Laos                   | 0.01%    | 0.00%    | 0.01%     |
| Mexico                 | 0.61%    | 0.05%    | 0.54%     |
| Nicaragua              | 0.06%    | 0.01%    | 0.05%     |
| Outlying-US(Guam-USVI-etc) | 0.02% | 0.00% | 0.02%     |
| Peru                   | 0.08%    | 0.01%    | 0.07%     |
| Philippines            | 0.20%    | 0.32%    | 0.22%     |
| Poland                 | 0.03%    | 0.02%    | 0.03%     |
| Portugal               | 0.06%    | 0.01%    | 0.05%     |
| Puerto-Rico            | 0.15%    | 0.04%    | 0.14%     |
| Scotland               | 0.01%    | 0.02%    | 0.01%     |
| South                  | 0.17%    | 0.03%    | 0.15%     |
| Taiwan                 | 0.04%    | 0.07%    | 0.04%     |
| Thailand               | 0.03%    | 0.00%    | 0.03%     |
| Trinadad&Tobago        | 0.06%    | 0.03%    | 0.06%     |
| United-States          | 89.16%   | 91.47%   | 89.63%    |
| Vietnam                | 0.07%    | 0.00%    | 0.06%     |
| Yugoslavia             | 0.01%    | 0.01%    | 0.01%     |

---

## 📉 Regression Analysis Summary

### Model Stats:
- **Multiple R**: 0.341
- **R-Squared**: 0.116
- **Adjusted R-Squared**: 0.116
- **Standard Error**: 0.4019
- **Observations**: 32,561

### ANOVA Table:

| Source     | df | SS       | MS        | F         | Significance F |
|------------|----|----------|-----------|-----------|----------------|
| Regression | 3  | 693.07   | 231.02    | 1429.99   | <0.0001        |
| Residual   | —  | —        | —         | —         | —              |

---

## 📊 Visualizations

- Bar Charts: Income by sex, education, occupation
- Map Charts: Income classification by country (planned)
- Histograms: Age and work hours distributions
- Heatmaps: Correlations between numerical features

---

## 🛠️ Tools & Technologies

- **Python**: pandas, seaborn, matplotlib, scikit-learn
- **Excel**: Pivot tables, country-wise summaries
- **Jupyter Notebook**: Analysis and visualization environment

---

## 🚀 Next Steps

- Improve model performance using ensemble methods (Random Forest, XGBoost)
- Explore fairness metrics (e.g., bias by sex or race)
- Create interactive dashboards (Plotly, Power BI, or Streamlit)
- Publish findings in a blog or deploy as a web app

---

## 👤 Author

**Nwabenu Great Imala**  
Data Analyst & Project Contributor

---

## 📉 Regression Analysis Summary

A multiple linear regression was conducted to examine the relationship between predictor variables (e.g., Age, Sex, Education) and income classification.

### 🔢 Model Summary:

| Metric              | Value     |
|---------------------|-----------|
| Multiple R          | 0.3412    |
| R Square            | 0.1164    |
| Adjusted R Square   | 0.1163    |
| Standard Error      | 0.4019    |
| Observations        | 32,561    |

---

### 📊 ANOVA Table:

| Source       | df  | SS        | MS         | F        | Significance F |
|--------------|-----|-----------|------------|----------|----------------|
| Regression   | 3   | 693.07    | 231.02     | 1429.99  | < 0.0001        |
| Residual     | —   | —         | —          | —        | —              |

---

### 🧠 Interpretation:

- **Model Significance**: The model is statistically significant (*p* < 0.0001), indicating that at least one predictor has a meaningful relationship with the income class.
- **R² Value**: An R² of 0.116 means that approximately 11.6% of the variation in income classification is explained by the model. This is modest, but common in social science and demographic data.
- **Predictor Influence**:
  - **Age**: Positively associated with higher income.
  - **Sex**: Gender differences were noted — males more likely to earn >50K.
  - **Education**: Higher education levels significantly increase the likelihood of earning >50K.

📌 *Note*: This statistical summary provides a foundation for model validation, but the model can be improved using more features and nonlinear or ensemble models.

