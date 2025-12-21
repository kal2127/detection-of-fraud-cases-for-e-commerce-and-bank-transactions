# Fraud Detection for E-commerce and Bank Transactions

## 📌 Project Overview
This project focuses on improving the detection of fraudulent transactions in both
e-commerce and banking domains. Fraud detection is a critical challenge due to the
highly imbalanced nature of transaction data, where fraudulent cases are rare but
carry significant financial risk.

The goal of this project is to build a robust, explainable fraud detection pipeline
that balances security and user experience by minimizing false positives while
accurately identifying fraudulent activity.

This project is part of the **10 Academy – Artificial Intelligence Mastery (Week 5 & 6 Challenge)**.

---

## 🎯 Objectives
- Explore and understand transaction datasets related to fraud detection
- Perform data cleaning and exploratory data analysis (EDA)
- Engineer meaningful behavioral, temporal, and geolocation-based features
- Analyze and address class imbalance in fraud datasets
- Build and evaluate machine learning models for fraud detection
- Interpret model predictions using explainable AI techniques (SHAP)

---

## 📂 Project Structure

```text
fraud-detection/
├── data/
│   ├── raw/                 # Original datasets (not tracked by Git)
│   └── processed/           # Cleaned and feature-engineered datasets
├── notebooks/
│   ├── eda-fraud-data.ipynb
│   ├── eda-creditcard.ipynb
│   ├── feature-engineering.ipynb
│   ├── modeling.ipynb
│   ├── shap-explainability.ipynb
│   └── README.md
├── models/                  # Saved trained models
├── src/                     # (Optional) reusable Python modules
├── tests/                   # Unit tests (if applicable)
├── requirements.txt
├── README.md
└── .gitignore

Datasets Used
1. Fraud_Data.csv (E-commerce Transactions)

User and transaction-level information

Includes timestamps, device, browser, source, IP address, and fraud label

Target variable: class

0 → Non-fraud

1 → Fraud

2. IpAddress_to_Country.csv

Maps IP address ranges to countries

Used for geolocation-based fraud analysis

3. creditcard.csv (Bank Transactions)

Anonymized credit card transaction data

Highly imbalanced fraud dataset

Target variable: Class

🔍 Work Completed (Interim-1)
✔ Data Cleaning & Preprocessing

Verified data types and handled timestamps

Checked and addressed duplicates and missing values

Converted IP addresses to integer format for range-based mapping

✔ Exploratory Data Analysis (EDA)

Analyzed class imbalance (≈ 90.6% non-fraud, 9.4% fraud)

Conducted univariate and bivariate analysis

Identified behavioral and transactional patterns linked to fraud

✔ Geolocation Analysis

Mapped IP addresses to countries using range-based lookup

Analyzed fraud rate variation across countries

✔ Feature Engineering

time_since_signup

hour_of_day

day_of_week

User-level transaction frequency

✔ Class Imbalance Strategy

Identified severe imbalance in fraud labels

Planned use of SMOTE applied only to training data during modeling

Selected appropriate evaluation metrics (Precision, Recall, F1, AUC-PR)

⚙️ Environment Setup
Requirements

All required dependencies are listed in requirements.txt.

Install them using:

pip install -r requirements.txt

Recommended Setup

It is recommended to use a virtual environment:

python -m venv venv
venv\Scripts\activate   # On Windows

📈 Next Steps (Task-2 & Task-3)

Data transformation (scaling and encoding)

Train-test split with stratification

Apply SMOTE on training data

Train baseline and ensemble models

Evaluate models using imbalanced classification metrics

Interpret predictions using SHAP

Provide business-oriented recommendations

📅 Key Deliverables

Interim-1: Data analysis, EDA, feature engineering ✔

Interim-2: Model building and evaluation

Final Submission: End-to-end pipeline with explainability and insights

👤 Author

Kalkidan
10 Academy – Artificial Intelligence Mastery Program

📄 License

This project is for educational purposes as part of the 10 Academy program.
