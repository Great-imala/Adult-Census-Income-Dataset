# Adult-Census-Income-Dataset
This dataset contains information about individuals from the 1994 US Census, with the goal of predicting whether a person's income exceeds $50,000 per year. The dataset includes demographic and employment information, such as age, education level, occupation, and work hours per week.
## Features:
•	Age: Continuous variable representing the individual's age.
•	Workclass: Categorical variable representing the individual's work class (e.g., Private, Self-emp-not-inc, etc.).
•	Fnlwgt: Continuous variable representing the individual's final weight.
•	Education: Categorical variable representing the individual's education level (e.g., HS-grad, Some-college, etc.).
•	Educational-num: Continuous variable representing the individual's educational number. 
•	Marital-status: Categorical variable representing the individual's marital status (e.g., Married-civ-spouse, Never-married, etc.).
•	Occupation: Categorical variable representing the individual's occupation (e.g., Machine-op-inspct, Adm-clerical, etc.).
•	Relationship: Categorical variable representing the individual's relationship (e.g., Husband, Wife, etc.).
•	Race: Categorical variable representing the individual's race (e.g., White, Black, etc.).
•	Gender: Categorical variable representing the individual's gender (e.g., Male, Female).
•	Capital-gain: Continuous variable representing the individual's capital gain.
•	Capital-loss: Continuous variable representing the individual's capital loss.
•	Hours-per-week: Continuous variable representing the individual's work hours per week.
•	Native-country: Categorical variable representing the individual's native country (e.g., United-States, Mexico, etc.).
•	Income: Binary variable representing whether the individual's income exceeds $50,000 per year (<=50K or >50K).
### Description of the Data:
The dataset contains 48,842 instances, but 32,562 of the data was use in the course of this study, with a mix of continuous and categorical variables. The data is mostly complete, with some missing values in the native-country feature. The income variable is imbalanced, with approximately 76% of instances having an income of <=50K and 24% having an income of >50K.
## Potential Use Questions:
•	Predicting individual income levels based on demographic and employment information (such as sex, educational level, marital status, occupation, race, country and age).
•	Does work hours determines individuals income?
•	Analyzing the relationships between hours-per-week, capital-gain and capital-loss on income.
