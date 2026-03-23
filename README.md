# Customer Churn Analysis & Feature Engineering

## Overview
This project focuses on analyzing customer behavior and predicting churn using machine learning techniques.  
A strong emphasis is placed on data preprocessing and feature engineering to extract meaningful patterns and improve model performance.

---

## Objectives
- Analyze customer behavior to identify patterns, trends, and key factors associated with churn  
- Perform data cleaning and preprocessing to ensure high-quality and consistent inputs  
- Engineer meaningful features that enhance model performance and capture customer usage patterns  
- Prepare structured training and testing datasets for machine learning modeling  
- Train predictive models to identify customers at risk of churn  
- Evaluate model performance using classification metrics and diagnostic tools (e.g., confusion matrix)  
- Validate model generalization through a proper train-test split  
- Establish a baseline model (Logistic Regression) for comparison with more advanced algorithms  

---

## Dataset

The project uses separate training and testing datasets:

- `customer_churn_dataset-training-master.csv`  
- `customer_churn_dataset-testing-master.csv`  

The dataset includes:
- Demographics  
- Customer engagement metrics  
- Financial behavior  
- Subscription details  

**Target Variable:**  
- `Churn` (1 = Churned, 0 = Retained)

---

## Data Preprocessing

### Data Cleaning
- Checked for missing values across all features  
- Applied appropriate handling (imputation or removal)  
- Converted categorical variables (e.g., Yes/No) into numerical format (1/0)  
- Removed irrelevant columns such as customer IDs  

### Data Validation
- Verified dataset structure and data types  
- Saved cleaned dataset for reproducibility:  
  `Data/Processed/Final_v_customer_churn_dataset.csv`

---

## Feature Engineering

Feature engineering was a key component of this project. Features were grouped and enhanced as follows:

### 1. Customer Engagement
- EngagementScore = Usage Frequency – Support Calls  
- Created EngagementLevel (Low / Medium / High)  
- Captures customer activity and interaction quality  

### 2. Financial Behavior
- AvgSpend = Total Spend / Tenure  
  Represents average customer value  

- LatePaymentFlag  
  - 1 if Payment Delay > 10 days  
  - 0 otherwise  
  Indicates potential financial risk  

### 3. Demographic Interaction
- Age × Gender interaction feature  
  Captures combined demographic effects  

### Feature Engineering Insights
- Highly engaged customers are less likely to churn  
- Customers with late payments show higher churn rates  
- Lower average spending is associated with higher churn risk  

---

## Exploratory Data Analysis (EDA)

EDA was conducted to validate feature relevance and uncover patterns.

Key visualizations:
- EngagementLevel vs Churn (bar chart)  
- AvgSpend vs Churn (boxplot)  
- LatePaymentFlag vs Churn (stacked bar chart)  

These insights guided feature engineering decisions and model development.

---

## Modeling

### Models Used
- Logistic Regression (baseline)  
- Random Forest  
- XGBoost  

### Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-score  

### Model Selection
- Priority was given to Recall to better identify churned customers  
- Random Forest achieved the best overall balance and was selected as the final model  

---

## Results
- The model successfully captured key churn patterns  
- Feature engineering significantly improved predictive performance  
- Random Forest demonstrated strong capability in identifying at-risk customers  
