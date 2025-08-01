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

