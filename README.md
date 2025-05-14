📉 Customer Churn Prediction Using Logistic Regression

Background

This project involves performing binary classification using logistic regression to predict customer churn for a telecommunications company. The dataset contains ~7,000 customer records with various attributes, including demographic information, service usage, and payment methods.

The goal is to preprocess and explore the dataset, identify key patterns influencing customer churn, and build a logistic regression model to predict whether a customer is likely to leave the service. This analysis also includes actionable business recommendations based on the model’s results.

Executive Summary

The objective of this project is to develop a logistic regression model that can accurately predict customer churn. The process involves cleaning and preparing the Telco dataset, encoding categorical features, exploring key relationships between variables and churn, and evaluating model performance using classification metrics and ROC analysis.

The final model helps identify high-risk customers and provides insight into which features most influence churn behavior — supporting proactive customer retention strategies.

🎯 Goals of Analysis
	•	Create and Clean DataFrame
Load the dataset and clean it by handling missing values, converting data types, and removing unnecessary columns.
	•	Data Exploration
Use visualizations and descriptive statistics to understand the churn distribution and feature relationships.
	•	Feature Engineering
Encode categorical variables and prepare the dataset for model training.
	•	Model Training
Train a logistic regression model using scikit-learn, and tune for convergence with max iteration settings.
	•	Model Evaluation
Evaluate model performance using accuracy, confusion matrix, classification report, and ROC AUC.
	•	Interpret Results
Analyze logistic regression coefficients to identify features with the highest impact on churn.

Methodology
	•	Data Retrieval: Loaded the Telco churn dataset from Kaggle.
	•	Data Cleaning:
	•	Converted TotalCharges to numeric and dropped missing values.
	•	Removed the customerID column.
	•	Feature Engineering:
	•	Applied one-hot encoding to all categorical variables.
	•	Created the binary Churn_Yes target variable.
	•	Train/Test Split: Split the data into 80% training and 20% testing sets.
	•	Modeling:
	•	Trained logistic regression with max_iter=3000.
	•	Used probability outputs for ROC analysis.
	•	Evaluation:
	•	Measured accuracy, precision, recall, and AUC.
	•	Visualized ROC curve for performance insight.
	•	Interpretation:
	•	Extracted and analyzed model coefficients.
	•	Identified key churn indicators.

Key Insights
	•	Month-to-Month Contracts are the most predictive of churn — customers on these plans are more likely to leave.
	•	Electronic Check Payment Method shows a high churn rate compared to credit card or automatic bank payments.
	•	Tenure and Long-Term Contracts are negatively associated with churn — long-time customers tend to stay.
	•	Higher Monthly Charges are linked to increased churn risk.
	•	The model achieved an AUC score of ~0.83, suggesting good discrimination between churners and non-churners.

Recommendations
	•	Promote Annual Plans: Convert month-to-month users to longer-term contracts through promotions.
	•	Encourage Auto-Pay: Incentivize switching from electronic check to credit card or bank transfer.
	•	Target New Customers: Offer loyalty perks to customers within their first year to reduce early churn.
	•	Monitor High-Bill Users: Identify and engage customers with high monthly charges to understand and reduce dissatisfaction.
