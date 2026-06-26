# 📊 Customer Churn Prediction, Retention & Customer Segmentation using Machine Learning

<div align="center">

### Predicting Customer Churn and Segmenting Customers for Data-Driven Retention Strategies

An end-to-end Machine Learning project that predicts customer churn, identifies key churn drivers, and segments customers into meaningful groups to help businesses improve customer retention.

</div>

---

# 📖 Table of Contents

* Project Overview
* Business Problem
* Objectives
* Dataset
* Tech Stack
* Project Workflow
* Exploratory Data Analysis
* Data Preprocessing
* Machine Learning Models
* Model Performance
* Feature Importance
* Customer Segmentation
* Business Recommendations
* Project Structure
* Installation
* Future Improvements
* Author

---

# 🌟 Project Overview

Customer churn is one of the biggest challenges faced by subscription-based businesses. Retaining existing customers is often more cost-effective than acquiring new ones. Predicting which customers are likely to leave enables organizations to take proactive steps that improve customer satisfaction and reduce revenue loss.

This project builds an end-to-end Machine Learning pipeline that predicts customer churn using Random Forest Classification, identifies the most influential churn factors, and segments customers using K-Means Clustering to support targeted retention strategies.

---

# 🎯 Business Problem

Telecommunication companies face customer attrition due to factors such as pricing, contract type, service quality, and technical support. The objective of this project is to:

* Predict customer churn using Machine Learning
* Identify the major factors contributing to churn
* Segment customers based on behavioral patterns
* Generate actionable business recommendations to improve customer retention

---

# 🎯 Project Objectives

* Perform Exploratory Data Analysis (EDA)
* Clean and preprocess telecom customer data
* Build multiple Random Forest models
* Handle class imbalance
* Optimize model performance using hyperparameter tuning
* Compare different model performances
* Analyze feature importance
* Perform customer segmentation using K-Means Clustering
* Translate insights into business recommendations

---

# 📂 Dataset

**Dataset:** IBM Telco Customer Churn Dataset

The dataset contains customer demographic information, subscribed services, contract details, billing information, payment methods, and churn status.

### Key Features

* Gender
* Senior Citizen
* Partner
* Dependents
* Tenure Months
* Phone Service
* Internet Service
* Contract Type
* Payment Method
* Monthly Charges
* Total Charges
* Tech Support
* Churn Value (Target)

---

# 🛠 Technology Stack

| Category                | Tools               |
| ----------------------- | ------------------- |
| Programming Language    | Python              |
| Data Analysis           | Pandas, NumPy       |
| Visualization           | Matplotlib, Seaborn |
| Machine Learning        | Scikit-Learn        |
| Clustering              | K-Means             |
| Development Environment | Google Colab        |

---

# 🔄 Project Workflow

```text
Dataset
   │
   ▼
Exploratory Data Analysis
   │
   ▼
Data Cleaning & Preprocessing
   │
   ▼
Feature Encoding
   │
   ▼
Random Forest Classification
   │
   ▼
Hyperparameter Tuning
   │
   ▼
Model Evaluation
   │
   ▼
Feature Importance Analysis
   │
   ▼
Customer Segmentation (K-Means)
   │
   ▼
Business Recommendations
```

---

# 📊 Exploratory Data Analysis

Key insights obtained during EDA include:

* Customers with shorter tenure are more likely to churn.
* Customers paying higher monthly charges exhibit higher churn rates.
* Month-to-Month contracts have the highest churn probability.
* Customers without Tech Support are more likely to leave.
* Payment methods influence customer retention behavior.

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed:

* Converted **Total Charges** to numeric format
* Handled missing values
* Removed identifier and location-related columns
* Removed data leakage features (Churn Label, Churn Score, CLTV)
* Applied One-Hot Encoding to categorical variables
* Split the dataset into training and testing sets using Stratified Sampling

---

# 🤖 Machine Learning Models

Three Random Forest models were implemented and compared.

### ✔ Baseline Random Forest

Standard Random Forest classifier trained using default parameters.

### ✔ Balanced Random Forest

Handled class imbalance using:

```python
class_weight='balanced'
```

### ✔ Tuned Random Forest

Optimized hyperparameters including:

* Number of Trees (`n_estimators`)
* Maximum Tree Depth (`max_depth`)

---

# 📈 Model Performance

| Model                  |   Accuracy |  Precision |     Recall |   F1 Score |
| ---------------------- | ---------: | ---------: | ---------: | ---------: |
| Baseline Random Forest | **96.52%** | **95.26%** | **91.44%** | **93.32%** |
| Balanced Random Forest | **92.26%** | **92.88%** | **76.74%** | **84.04%** |
| Tuned Random Forest    | **84.17%** | **65.70%** | **84.49%** | **73.92%** |

### Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* Classification Report
* Confusion Matrix
* Cross Validation

---

# ⭐ Feature Importance

Random Forest Feature Importance identified the most influential variables contributing to customer churn.

Top predictive features include:

* Tenure Months
* Monthly Charges
* Total Charges
* Contract Type
* Tech Support
* Payment Method

These insights help businesses understand which customer characteristics have the greatest impact on retention.

---

# 👥 Customer Segmentation

K-Means Clustering was applied to group customers into three meaningful behavioral segments.

### 🟢 Budget Loyal Customers

* Lower monthly charges
* Long-term customers
* Low churn probability

**Business Strategy**

* Reward customer loyalty
* Promote value-added services
* Maintain competitive pricing

---

### 🟠 High-Risk New Customers

* Short tenure
* Higher churn probability

**Business Strategy**

* Personalized onboarding
* Welcome offers
* Early customer engagement
* Proactive technical support

---

### 🔵 Loyal Premium Customers

* Long tenure
* Higher monthly spending
* Strong customer loyalty

**Business Strategy**

* Premium loyalty programs
* Exclusive offers
* Dedicated customer support
* Personalized recommendations

---

# 💼 Business Recommendations

### High-Risk Customers

* Encourage long-term contracts
* Improve onboarding experience
* Offer introductory discounts
* Provide free technical support trials

### Loyal Customers

* Launch customer loyalty programs
* Offer personalized promotions
* Increase customer engagement through exclusive benefits

### Overall Business Strategy

* Monitor customers with short tenure
* Reduce churn among Month-to-Month contract customers
* Improve customer support quality
* Implement targeted retention campaigns using customer segmentation

---

# 📁 Project Structure

```text
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction.ipynb
├── Telco_customer_churn.xlsx
├── confusion_matrix.png
├── feature_importance.png
├── README.md
└── requirements.txt
```

---

# ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/customer-churn-prediction.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook
```

---

# 🚀 Future Improvements

* Compare additional models such as XGBoost, LightGBM, and CatBoost
* Perform advanced feature engineering
* Build an interactive Streamlit dashboard
* Deploy the model using Flask or FastAPI
* Use SHAP values for explainable AI (XAI)
* Automate hyperparameter tuning with GridSearchCV or Optuna

---

# 👨‍💻 Author

**Your Name**

Aspiring Data Scientist | Machine Learning Enthusiast | Python Developer

If you found this project useful, consider giving it a ⭐ on GitHub!
