Loan Default Prediction using Random Forest

A Machine Learning Classification Project

📝 Project Overview

This project predicts whether a borrower will fail to fully repay a loan (not.fully.paid) using historical Lending Club data.
A Random Forest Classifier is used because it handles non-linear relationships, mixed feature types, missing values, and provides strong baseline performance.

The goal is to help financial institutions assess loan default risk.

🎯 Objectives

Explore and understand loan borrower behavior

Clean and preprocess numeric + categorical variables

Train a Random Forest model to predict not.fully.paid

Evaluate the model using classification metrics

Identify the most important features influencing loan default

📂 Dataset Description
File: loan_data.csv

Your dataset contains the following features:

Column	Description
credit.policy	Borrower meets the bank's credit policy (1 = Yes, 0 = No)
purpose	Reason for loan (credit_card, debt_consolidation, etc.)
int.rate	Interest rate (as a decimal)
installment	Monthly loan payment
log.annual.inc	Log of the annual income
dti	Debt-to-income ratio
fico	FICO credit score
days.with.cr.line	Number of days the borrower has had a credit line
revol.bal	Revolving balance
revol.util	Revolving line utilization rate
inq.last.6mths	Number of credit inquiries in last 6 months
delinq.2yrs	Number of delinquencies in last 2 years
pub.rec	Number of derogatory public records
not.fully.paid	Target Variable – 1 = default, 0 = paid
🔧 Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib / Seaborn

Random Forest Classifier

🔍 Steps Performed
1. Exploratory Data Analysis (EDA)

Checked missing values

Visualized numeric distributions

Studied skewness and used log1p where necessary

Checked correlations

Analyzed categorical variable purpose

2. Preprocessing

Encoding categorical feature (purpose) using One-Hot Encoding

Standardizing numeric features

Splitting dataset into train/test

Handling skewed features (log1p transformation)

3. Model Building

Random Forest Classifier:

from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=300,
    max_depth=None,
    random_state=42
)
model.fit(X_train, y_train)

4. Model Evaluation

Metrics used:

Accuracy

Precision

Recall

F1 Score

Confusion Matrix

ROC-AUC Score

Feature Importance Plot

📈 Results

Expected performance on this dataset:

Accuracy: ~80–88%

Precision & Recall: Balanced

Top Feature Importances:

fico

int.rate

credit.policy

dti

installment
