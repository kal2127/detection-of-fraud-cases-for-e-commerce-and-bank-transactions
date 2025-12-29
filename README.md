Fraud Detection for E-Commerce and Banking Transactions

Project Overview

Fraud detection is a critical challenge in financial and e-commerce systems due to the
significant financial losses caused by fraudulent transactions and the highly
imbalanced nature of fraud data. In such datasets, fraudulent transactions represent
only a small fraction of total transactions, making traditional evaluation metrics
like accuracy unreliable.

This project aims to build an end-to-end fraud detection pipeline that:

Identifies fraudulent transactions effectively

Minimizes disruption to legitimate customers

Provides transparent and explainable model decisions

The project follows best practices in data analysis, machine learning modeling,
imbalance handling, and model explainability.

This work is part of the 10 Academy – Artificial Intelligence Mastery Program
(Week 5 & 6 Challenge).

🎯 Project Objectives

Perform exploratory data analysis (EDA) on fraud datasets

Engineer meaningful temporal, behavioral, and geolocation features

Handle severe class imbalance appropriately

Train and evaluate machine learning models for fraud detection

Compare baseline and ensemble models

Explain model predictions using SHAP

Provide insights suitable for business and regulatory contexts

📂 Project Structure

fraud-detection/
├── data/
│ ├── raw/ # Original datasets (excluded from Git)
│ └── processed/ # Cleaned and feature-engineered datasets
├── notebooks/
│ ├── eda-fraud-data.ipynb
│ ├── eda-creditcard.ipynb
│ ├── feature-engineering.ipynb
│ ├── modeling.ipynb
│ └── shap-explainability.ipynb
├── models/ # Saved trained models
├── src/ # Optional reusable scripts
├── requirements.txt
├── README.md
└── .gitignore

📊 Datasets
1️⃣ E-Commerce Fraud Dataset (Fraud_Data.csv)

User demographic information

Transaction details (purchase value, device, browser, source)

Signup and purchase timestamps

IP address information

Target variable: class

0 → Legitimate transaction

1 → Fraudulent transaction

2️⃣ IP-to-Country Dataset (IpAddress_to_Country.csv)

Maps IP address ranges to countries

Used for geolocation-based fraud analysis

3️⃣ Credit Card Fraud Dataset (creditcard.csv)

Anonymized banking transactions

Extremely imbalanced fraud labels

Target variable: Class

🔍 Task-1: Exploratory Data Analysis & Feature Engineering
✔ Data Cleaning

Verified data types and timestamp formats

Handled missing values and duplicates

Converted IP addresses to integer format for range-based mapping

✔ Exploratory Data Analysis (EDA)

Conducted univariate and bivariate analysis

Identified severe class imbalance (≈ 90.6% non-fraud, 9.4% fraud)

Analyzed relationships between fraud and purchase value, browser, source, and country

✔ Feature Engineering

time_since_signup

hour_of_day

day_of_week

User transaction frequency

Country feature derived from IP mapping

✔ Class Imbalance Analysis

Confirmed that accuracy is not suitable for fraud detection

Identified the need for resampling and precision-recall-based evaluation

🤖 Task-2: Model Building & Evaluation
✔ Data Preparation

Stratified train-test split to preserve class distribution

Separation of features (X) and target variable (y)

✔ Data Transformation

One-Hot Encoding for categorical features

Feature scaling using StandardScaler

All transformations fitted on training data only to prevent data leakage

✔ Handling Class Imbalance

Applied SMOTE to training data only

Documented class distribution before and after resampling

Justified SMOTE as appropriate for minority fraud learning

✔ Models Trained
1️⃣ Logistic Regression (Baseline Model)

Simple and interpretable

Used as a benchmark for performance comparison

2️⃣ Random Forest (Ensemble Model)

Captures non-linear feature interactions

Better performance on complex fraud patterns

✔ Model Evaluation Metrics

Due to class imbalance, the following metrics were used:

Precision

Recall

F1-Score

Area Under Precision-Recall Curve (AUC-PR)

Confusion Matrix

Accuracy was not used as a primary evaluation metric.

✔ Model Selection

Logistic Regression offered interpretability but limited performance

Random Forest achieved stronger recall and F1-score

Trade-off between explainability and predictive power was analyzed

Random Forest was selected as the preferred model

🔎 Task-3: Model Explainability (SHAP)
✔ Explainability Goals

Understand why transactions are classified as fraud

Identify key drivers of fraud predictions

Provide transparency for business and regulatory requirements

✔ SHAP Analysis

Global feature importance using SHAP summary plots

Individual prediction explanations using SHAP waterfall/force plots

Feature effect analysis using SHAP dependence plots

✔ Key Insights

High purchase value and short time since signup significantly increase fraud risk

Geolocation and behavioral features play a strong role in predictions

Model decisions align with real-world fraud patterns

⚙️ Setup Instructions
1️⃣ Create a Virtual Environment (Recommended)
python -m venv venv

Activate:

Windows

venv\Scripts\activate

Linux / macOS

source venv/bin/activate

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Run Notebooks

Launch Jupyter:

jupyter notebook

Run notebooks in this order:

eda-fraud-data.ipynb

feature-engineering.ipynb

modeling.ipynb

shap-explainability.ipynb

📈 Key Takeaways

Fraud detection requires specialized handling of imbalanced data

Precision-Recall metrics are essential for proper evaluation

Ensemble models outperform linear baselines in fraud scenarios

Explainability is critical for trust and deployment readiness

🚀 Future Improvements

Hyperparameter tuning for ensemble models

Cost-sensitive learning

Real-time fraud detection pipeline

Deployment using REST APIs

👤 Author

Kalkidan Tesfaye
10 Academy – Artificial Intelligence Mastery Program

📄 License

This project is developed for educational purposes as part of the 10 Academy program.
