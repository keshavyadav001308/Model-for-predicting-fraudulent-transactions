Fraud Detection in Financial Transactions using Machine Learning

 Project Overview

This project focuses on building an end-to-end **fraud detection system** for financial transactions using machine learning.  
The objective is to accurately identify fraudulent transactions while minimizing false positives and converting model insights into **practical fraud prevention strategies**.

The dataset represents real-world financial behavior and contains over **6.3 million transactions**, making this a large-scale and highly imbalanced classification problem.

Business Problem

Financial fraud leads to major revenue loss and reduced customer trust.  
The goal of this project is to:

- Detect fraudulent transactions proactively  
- Reduce fraud-related financial losses  
- Maintain a smooth experience for genuine customers  
- Provide actionable insights to improve fraud prevention infrastructure  

Dataset Information

- **Total Rows:** 6,362,620  
- **Total Columns:** 10  
- **Target Variable:** `isFraud`

### Key Features
- `step` – Time unit (1 step = 1 hour)
- `type` – Transaction type
- `amount` – Transaction amount
- `oldbalanceOrg`, `newbalanceOrig` – Sender balances
- `oldbalanceDest`, `newbalanceDest` – Receiver balances
- `isFraud` – Fraud label (1 = Fraud, 0 = Not Fraud)
- `isFlaggedFraud` – Rule-based fraud flag

 Project 
STEP 1: Data Cleaning & Feature Engineering
- Handled implicit missing values for merchant transactions
- Applied log transformation to handle outliers in transaction amounts
- Created balance consistency features to capture abnormal behavior
- One-hot encoded transaction types
- Removed high-cardinality ID columns
- Verified extreme class imbalance (~0.13% fraud)

STEP 2: Model Development
- Built a Random Forest classifier
- Used class weighting to handle imbalanced data
- Applied stratified train-test split
- Generated fraud probability scores

STEP 3: Feature Selection
- Used model-based feature importance
- Selected behavior-driven features
- Removed low-impact variables (optional)

 STEP 4: Model Evaluation
Because accuracy is misleading for imbalanced data, the following metrics were used:
- Confusion Matrix
- Precision, Recall, F1-score
- ROC-AUC
- Precision-Recall Curve

STEP 5: Key Fraud Indicators
- Transaction type (TRANSFER, CASH_OUT)
- Large transaction amounts
- Balance inconsistencies
- Sudden account depletion
- Customer-to-customer transfers

STEP 6: Business Validation
The identified fraud patterns align with real-world financial fraud behavior, making the model reliable and explainable.

STEP 7: Fraud Prevention Strategy
- Real-time transaction monitoring
- Risk-based decision thresholds
- Dynamic transaction limits
- Multi-factor authentication
- Velocity and pattern monitoring
- Temporary account freezing
- Continuous model retraining

STEP 8: Measuring Effectiveness
- Reduction in fraud rate and financial loss
- Recall and precision monitoring
- False positive rate
- Customer complaints
- A/B testing and controlled experiments

 Models Implemented

- Logistic Regression
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM
- CatBoost

Models were compared using **ROC-AUC and Recall**.

Technologies Used

- **Programming Language:** Python  
- **Libraries:**  
  - pandas  
  - numpy  
  - scikit-learn  
  - matplotlib  
  - xgboost  
  - lightgbm  
  - catboost  


## 📁 Project Structure

