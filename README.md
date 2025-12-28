# detection-of-fraud-cases-for-e-commerce-and-bank-transactions
Project Overview

Fraud detection is a critical problem in financial and e-commerce systems due to the
high cost of fraudulent activities and the highly imbalanced nature of transaction data.
This project aims to build robust and explainable machine learning models that can
effectively identify fraudulent transactions while minimizing disruption to legitimate
customers.

The project follows an end-to-end machine learning workflow, including exploratory
data analysis, feature engineering, class imbalance handling, model training, and
evaluation using appropriate metrics for imbalanced classification.

This work is part of the 10 Academy – Artificial Intelligence Mastery Program
(Week 5 & 6 Challenge).

🎯 Project Objectives

Explore and understand fraud-related transaction datasets

Perform data cleaning and exploratory data analysis (EDA)

Engineer meaningful temporal, behavioral, and geolocation-based features

Analyze and handle severe class imbalance

Train and evaluate machine learning models for fraud detection

Compare baseline and ensemble models using appropriate metrics

Select a model that balances fraud detection performance and customer experience

📂 Project Structure
fraud-detection/
├── data/
│   ├── raw/                     # Original datasets (not tracked)
│   └── processed/               # Cleaned & feature-engineered datasets
├── notebooks/
│   ├── eda-fraud-data.ipynb
│   ├── eda-creditcard.ipynb
│   ├── feature-engineering.ipynb
│   ├── modeling.ipynb
│   └── shap-explainability.ipynb
├── models/                      # Saved trained models
├── src/                         # Reusable scripts (optional)
├── requirements.txt
├── README.md
└── .gitignore

📊 Datasets
1️⃣ Fraud_Data.csv (E-Commerce Transactions)

User demographics and transaction details

Device, browser, source, IP address

Timestamped signup and purchase events

Target variable: class

0 → Non-fraud

1 → Fraud

2️⃣ IpAddress_to_Country.csv

Maps IP address ranges to countries

Used for geolocation-based fraud analysis

3️⃣ creditcard.csv (Bank Transactions)

Anonymized credit card transactions

Highly imbalanced fraud dataset

Target variable: Class

🔍 Task-1: Exploratory Data Analysis & Feature Engineering
✔ Data Cleaning

Verified data types and timestamp formats

Handled duplicates and missing values

Converted IP addresses to integer format for range-based mapping

✔ Exploratory Data Analysis (EDA)

Identified severe class imbalance (≈ 90.6% non-fraud, 9.4% fraud)

Conducted univariate and bivariate analysis

Analyzed fraud patterns across purchase value, browser, source, and country

✔ Geolocation Analysis

Mapped transactions to countries using IP address ranges

Observed significant variation in fraud rates across countries

✔ Feature Engineering

time_since_signup

hour_of_day

day_of_week

User-level transaction frequency

Geolocation features derived from IP mapping

✔ Class Imbalance Analysis

Confirmed that accuracy is not a reliable metric

Planned resampling strategy for modeling stage

🤖 Task-2: Model Building & Evaluation
✔ Data Preparation

Stratified train-test split to preserve fraud ratio

Separation of features (X) and target (y)

Documented class distribution before resampling

✔ Data Transformation

One-Hot Encoding for categorical features

Feature scaling using StandardScaler

Transformations fitted on training data only to avoid data leakage

✔ Handling Class Imbalance

Applied SMOTE to training data only

Documented class distribution before and after resampling

Justified SMOTE as suitable for minority fraud class learning

✔ Models Trained
1️⃣ Logistic Regression (Baseline)

Simple and interpretable baseline model

Used to understand feature impact and establish reference performance

2️⃣ Random Forest (Ensemble Model)

Captures non-linear relationships

More robust to complex fraud patterns

Demonstrated improved performance over baseline

✔ Model Evaluation Metrics

Due to class imbalance, the following metrics were used:

Precision

Recall

F1-Score

Area Under Precision-Recall Curve (AUC-PR)

Confusion Matrix

Accuracy was intentionally avoided as a primary metric.

✔ Model Comparison & Selection

Logistic Regression provided interpretability but limited performance

Random Forest achieved better recall and F1-score for fraud detection

Trade-off between explainability and predictive power was analyzed

Random Forest selected as the preferred model for fraud detection

⚙️ Environment Setup
Requirements

All dependencies are listed in requirements.txt.

Install with:

pip install -r requirements.txt

Recommended Virtual Environment
python -m venv venv
venv\Scripts\activate   # Windows

📈 Key Takeaways

Fraud detection requires careful handling of class imbalance

Precision-Recall based metrics are more informative than accuracy

Ensemble models outperform linear baselines for complex fraud patterns

Model decisions must balance fraud prevention and customer experience

🚀 Next Steps (Task-3)

Model explainability using SHAP

Feature importance interpretation

Business-oriented insights and recommendations

Final model reporting and documentation

👤 Author

Kalkidan Tesfaye
10 Academy – Artificial Intelligence Mastery Program
