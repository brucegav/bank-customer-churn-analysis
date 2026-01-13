# Project Overview

This project analyzes a dataset of 10,000 bank customers to identify key drivers of churn.  I performed extensive data cleaning, exploratory data analysis, and feature engineering before building a Random Forest Classifier to predict at-risk customers.

## Key Insights

Through EDA, I discovered several critical factors influencing churn:

- Age: Churn probability increases significantly for customers between the ages of 40 and 60.
- Product Overload: Customers holding 3 or more products have a near -100% churn rate, suggesting a potential friction point in multi-product service.
- Geographic Trends: German customers are nearly twice as likely to churn compared to those in France or Spain.
- Irrelevant Metrics: Surprisingly, customer tenure and salary showed almost no correlation with the decision to leave.


## Data Preparation and Feature Engineering

To prepare the data for machine learning, I:

- Cleaned inconsistent labels for 'France'
- Converted object-based currency strings to numeric floats
- Converted object-based columns to numeric (where appropriate)
- Transformed 'Geography' and 'Gender' (categorical features) into dummy variables
- Created a new feature, 'balance_v_income', which is a ratio to measure the depth of the financial relationship relative to earnings


## Model Performance

I utilized a Random Forest Classifier to establish a baseline for prediction.

- Accuracy: 85.85%
- Confusion Matrix Insights: The model is currently highly precise but conservative in identifying churners.  This provides a clear roadmap for future optimization using threshold adjustments or SMOTE.


## How to Use

1. Clone this repository
2. Install dependencies: pip install pandas seaborn scikit-learn matplotlib
3. Open Bank_Churn_Analysis.ipynb in Jupyter Notebook or VS Code