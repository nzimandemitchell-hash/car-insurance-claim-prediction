# Car Insurance Claim Prediction

## Project Overview

This project uses customer, vehicle, and driving-history data to analyze and predict car insurance claim outcomes.

The project follows an end-to-end data analytics and machine learning workflow, including data quality checks, missing-value treatment, exploratory data analysis, feature preprocessing, model development, and evaluation.

A Logistic Regression model was developed to predict whether a customer would make an insurance claim.

---

##  Business Problem

Insurance companies need to understand factors associated with customer claim outcomes so they can better analyze risk and support data-driven decision-making.

The objective of this project is to:

* Explore customer and vehicle characteristics associated with insurance claims.
* Identify patterns in driving history and claim outcomes.
* Prepare the dataset for machine learning.
* Develop a classification model to predict claim outcomes.
* Evaluate the model's performance against a simple baseline.

---

## Dataset

The dataset contains **10,000 customer records** and **18 variables** covering customer demographics, vehicle information, driving history, and insurance claim outcomes.

### Key variables include:

* Age group
* Gender
* Driving experience
* Education
* Income
* Credit score
* Vehicle ownership
* Vehicle year
* Marital status
* Children
* Postal code
* Annual mileage
* Vehicle type
* Speeding violations
* DUI history
* Previous accidents
* Insurance claim outcome

The target variable is:

**`outcome`**

* `0` = No claim
* `1` = Claim

---

## Data Preparation

The following data preparation steps were performed:

* Checked dataset dimensions and data types.
* Investigated missing values.
* Checked for duplicate records and duplicate IDs.
* Examined categorical and numerical variables.
* Investigated the relationship between missing values and claim outcomes.
* Applied median imputation to missing `credit_score` values.
* Applied median imputation to missing `annual_mileage` values.
* Removed the `id` column from the modelling features.

After cleaning, the dataset contained **10,000 records with no missing values**.

---

## Exploratory Data Analysis

Exploratory analysis was performed to investigate claim patterns across different customer and driving characteristics.

The analysis included:

* Claim rate by age group
* Claim rate by driving experience
* Claim rate by previous accidents
* Claim rate by speeding violations
* Claim rate by income
* Claim rate by vehicle type
* Numerical variable distributions

These analyses were used to identify patterns that could be useful for understanding insurance claim behaviour.

---

##  Machine Learning

### Model

A **Logistic Regression** classification model was selected as the initial predictive model.

The modelling workflow included:

1. Separating features and target variable.
2. Removing the customer ID.
3. Splitting the data into training and testing sets.
4. Using stratified sampling to preserve the target-class distribution.
5. One-hot encoding categorical variables.
6. Standardising numerical variables.
7. Training the Logistic Regression model.
8. Generating predictions on the test dataset.

### Train/Test Split

* Training data: **80%**
* Testing data: **20%**
* Random state: `42`
* Stratification: Applied to the target variable

---

##  Model Performance

The Logistic Regression model achieved:

| Metric                  |     Result |
| ----------------------- | ---------: |
| Test Accuracy           | **83.60%** |
| Majority-Class Baseline | **68.67%** |

The model's test accuracy was higher than the baseline that would result from always predicting the majority class.

> **Note:** Accuracy alone does not fully describe classification performance, particularly when the target classes are imbalanced. The dataset contains approximately 68.67% non-claim outcomes and 31.33% claim outcomes.

---

##  Business Insights

The exploratory analysis was used to investigate how claim outcomes varied across:

* Customer age groups
* Driving experience
* Previous accident history
* Speeding violations
* Income groups
* Vehicle types

These comparisons provide a business-oriented view of the factors associated with insurance claim outcomes.

The analysis should be interpreted as identifying **associations rather than proving causation**.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Google Colab**
* **Jupyter Notebook**

---

## Future Improvements

Potential future improvements include:

* Comparing Logistic Regression with additional classification algorithms.
* Hyperparameter tuning.
* More detailed feature engineering.
* Threshold optimisation based on business requirements.
* Adding model explainability techniques.
* Developing a Power BI dashboard to communicate the analysis visually.

---

# Project Outcome

This project strengthened my practical experience in:

* Data cleaning
* Exploratory data analysis
* Feature preprocessing
* Classification modelling
* Model evaluation
* Business-oriented data interpretation

It demonstrates an end-to-end approach to using Python and machine learning to investigate a real-world-style business problem.
