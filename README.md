# 🏥 Insurance Cost Analysis – Data Exploration & Modeling

## 📋 Overview
This project explores a **medical insurance dataset** to understand what affects insurance charges.  
We analyze factors like **age, gender, BMI, smoking habits, and region**, perform **data cleaning**, **exploratory analysis**, and build **regression models** to predict charges.  

[Insurance Cost Analysis Notebook](./Data-Analytics-for-Insurance-Cost-Data-Set.ipynb)

Technologies used: **Python, Pandas, Numpy, Seaborn, Matplotlib, Scikit-learn**.

---

## 1️⃣ Task 1: Import Dataset & Initial Exploration
- Dataset loaded from CSV and first 10 rows displayed.
- Column headers renamed to: `['age','gender','bmi','no_of_children','smoker','region','charges']`.
- Missing values (`?`) replaced with `NaN`.

**Purpose:** Understand the dataset structure and identify missing data.

---

## 2️⃣ Task 2: Data Wrangling
- **Identify missing values** using `df.info()`.
- **Handle missing data**:
  - Continuous: Replace missing `age` with mean.  
  - Categorical: Replace missing `smoker` with most frequent value.
- **Update data types** for `age` and `smoker`.
- **Round `charges`** to 3 decimals for clarity.

**Purpose:** Ensure the dataset is clean, consistent, and ready for analysis.

---

## 3️⃣ Task 3: Exploratory Data Analysis (EDA)

### Age Distribution
<img src="img/age_distribution.png" width="500"/>

- Most policyholders are aged 18–40.  
- Age moderately affects insurance charges: older policyholders tend to have higher costs.

### Gender Distribution
<img src="img/gender_distribution.png" width="500"/>

- Male and female counts are fairly balanced.  
- Gender alone has little impact on charges.

### Charges Distribution
<img src="img/charges_distribution.png" width="500"/>

- Most people pay low to moderate insurance costs.  
- A small number of people have very high costs, which makes the overall distribution uneven.  


### Log-Transformed Charges
<img src="img/log_charges_distribution.png" width="500"/>

- Log transformation reduces skewness and makes patterns clearer for modeling.  

### Charges by Smoker Status
<img src="img/charges_by_smoker.png" width="500"/>

- Smokers pay significantly more than non-smokers. 🚬💸  
- Smoking is the strongest single predictor of higher insurance charges.

### Charges vs BMI
<img src="img/charges_vs_bmi.png" width="500"/>

- Higher BMI generally increases charges, but the relationship is not perfectly linear. ⚖️  

### Charges vs Smoker (Regression)
<img src="img/charges_vs_smoker.png" width="500"/>

- Reinforces that smokers have much higher charges than non-smokers. ✅  

**EDA Conclusion:**  
From the plots, the most important factors influencing insurance costs are **smoking status, BMI, and age**, while gender and region have smaller effects. Patterns observed here inform the modeling strategy in the next steps.

---

## 4️⃣ Task 4: Model Development

- Built **Linear Regression models**: first simple (`charges ~ smoker`), then multiple features (`age, gender, BMI, no_of_children, smoker, region`).  
- Applied a **Pipeline** with scaling and polynomial features.  
- Predicted charges and evaluated performance with **R² score**.

**Task 4 Conclusion:**  
- Linear Regression confirms that **smoking status and BMI are strong predictors**.  
- Age contributes moderately.  
- The model fits well on the dataset, but some variability remains due to outliers (very high charges) and non-linear effects.

---

## 5️⃣ Task 5: Model Refinement

- Split dataset into **training (80%) and testing (20%)**.  
- Applied **Ridge Regression** to reduce overfitting from multiple correlated features.  
- Evaluated performance on the test set using **R² score**.
-Our regression model predicts insurance charges accurately! Most predicted values are very close to the actual charges. (See chart below)
<img src="img/predicted_vs_actual.png" width="500"/>

**Task 5 Conclusion:**  
- Ridge Regression improves generalization and stabilizes predictions.  
- Confirms that **smoking, BMI, and age remain the main drivers** of charges.  
- Using Ridge helps handle feature correlations and slightly reduces error compared to simple linear regression.

---

## 📝 Final Conclusion

- **Key Drivers:** Smoking status 🚬, BMI ⚖️, and age are the main determinants of insurance cost.  
- **Modeling Insight:** Linear and Ridge Regression show similar patterns, but Ridge better handles correlated features and avoids overfitting.  
- **Other Features:** Gender, number of children, and region have less influence but can complement the model.  

**Bottom line:** Smoking is the single strongest factor, followed by BMI and age. These insights can guide insurance pricing and risk prediction, while the modeling pipeline provides a solid foundation for predictive analysis.
