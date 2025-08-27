# 🏥 Insurance Cost Analysis – Data Exploration & Visualization

## 📋 Overview
This project explores a **medical insurance dataset** to understand what affects insurance charges.  
We analyze factors like **age, gender, BMI, smoking habits, and region**. Using **Python, Pandas, Seaborn, and Matplotlib**, we clean the data, explore trends, and visualize patterns to gain insights.  

---

## 📊 Files / Plots

### 1️⃣ `age_distribution.png`  
- **What it shows:** The age distribution of policyholders.  
- **Explanation:** Most people are between 18–40 years old, with a few older participants.  
- **Takeaway:** Age matters for insurance costs—older people usually pay more.  

---

### 2️⃣ `gender_distribution.png`  
- **What it shows:** Count of male vs female policyholders.  
- **Explanation:** Gender is fairly balanced in this dataset.  
- **Takeaway:** Gender alone doesn’t hugely affect charges, but it’s worth keeping in mind.  

---

### 3️⃣ `charges_distribution.png`  
- **What it shows:** How insurance charges are spread across policyholders.  
- **Explanation:** Most pay lower premiums, but a few high-cost cases stretch the distribution.  
- **Takeaway:** A few very expensive cases influence averages significantly.  

---

### 4️⃣ `log_charges_distribution.png`  
- **What it shows:** Log-transformed charges distribution.  
- **Explanation:** Log transformation reduces skewness and makes the data easier to model.  
- **Takeaway:** Useful for statistical analysis and predictive modeling.  

---

### 5️⃣ `charges_by_smoker.png`  
- **What it shows:** Boxplot of charges for smokers vs non-smokers.  
- **Explanation:** Smokers clearly pay much higher charges.  
- **Takeaway:** Smoking is a major factor in predicting insurance costs. 🚬💸  

---

### 6️⃣ `charges_vs_bmi.png`  
- **What it shows:** Charges vs BMI scatter plot with regression line.  
- **Explanation:** Higher BMI is linked to higher charges, though the relationship isn’t perfect.  
- **Takeaway:** BMI is another important factor in insurance cost prediction. ⚖️  

---

### 7️⃣ `charges_vs_smoker.png`  
- **What it shows:** Regression of charges vs smoker status (numeric).  
- **Explanation:** Again confirms that smokers pay more.  
- **Takeaway:** Smoking status is a key predictor. ✅  

---

## 📝 Conclusion
From the visualizations:  

- **Age**: Older people generally pay more.  
- **Smokers**: Have significantly higher charges than non-smokers.  
- **BMI**: Higher BMI increases costs moderately.  
- **Gender & Region**: Less impactful individually but can be part of a model.  

**Bottom line:** Smoking and BMI are the strongest drivers of insurance cost, with age also playing a role. This analysis sets the stage for building predictive models for estimating charges.  
