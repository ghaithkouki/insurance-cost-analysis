# Insurance Cost Analysis Project

This project involves analyzing insurance data and building regression models to predict insurance charges.

## Notebook

You can view the full Jupyter notebook here:

[Insurance Cost Analysis Notebook](./Data-Analytics-for-Insurance-Cost-Data-Set.ipynb)

## Data Wrangling and Exploration

### Age Distribution
This is the histogram showing the distribution of the `age` column in the dataset.

![Age Distribution](./images/age_distribution.png)

### Gender Distribution
Here we show the gender distribution in the dataset.

![Gender Distribution](./images/gender_distribution.png)

### Charges Distribution
The histogram below shows the distribution of the `charges` column, which represents the insurance charges.

![Charges Distribution](./images/charges_distribution.png)

### Log-Transformed Charges Distribution
Here we plot the log-transformed distribution of the `charges` column.

![Log-Transformed Charges Distribution](./images/log_charges_distribution.png)

### Charges by Smoker Status
This boxplot visualizes the charges for people who smoke vs. those who don’t.

![Charges by Smoker Status](./images/charges_by_smoker.png)

### BMI vs Charges
The following regression plot shows the relationship between `BMI` and insurance `charges`.

![BMI vs Charges](./images/bmi_vs_charges.png)

### Smoker vs Charges
This regression plot shows the relationship between `smoker` status and insurance charges.

![Smoker vs Charges](./images/smoker_vs_charges.png)

### Correlation Matrix
Here’s the correlation matrix of the features in the dataset.

![Correlation Matrix](./images/correlation_matrix.png)

## Model Development

We created regression models using the features of the dataset to predict `charges`:

- **Linear Regression Model**: This model uses the `smoker` attribute to predict `charges` and achieves an R-squared value of X.
- **Multiple Linear Regression Model**: We expanded the model to include multiple features and achieved a better performance.
- **Polynomial Regression**: We used polynomial features to improve the model further, resulting in an even higher R-squared score.

## Model Refinement

We split the data into training and testing subsets and applied Ridge Regression to refine the model's performance. The Ridge model achieved an R-squared score of Y on the testing dataset.

### Ridge Regression Performance
We used Ridge regression to improve model performance and the R-squared score was X.

