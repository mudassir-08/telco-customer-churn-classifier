# Telco Customer Churn Prediction — End-to-End Machine Learning Pipeline


<!-- CORE STACK -->
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-End--to--End%20Pipeline-8E44AD?style=for-the-badge)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Framework-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-Boosting%20Model-1E8449?style=for-the-badge)

---

<!-- DATA + ENGINEERING -->
![Pandas](https://img.shields.io/badge/Pandas-Data%20Engineering-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pipeline](https://img.shields.io/badge/ML%20Pipeline-Production%20Ready-2E86C1?style=for-the-badge)

---

<!-- BUSINESS FOCUS -->
![Business Problem](https://img.shields.io/badge/Focus-Customer%20Churn%20Prediction-E74C3C?style=for-the-badge)
![Recall Optimized](https://img.shields.io/badge/Metric-Recall%20Focused-FF6B6B?style=for-the-badge)
![Imbalanced Data](https://img.shields.io/badge/Challenge-Class%20Imbalance-F39C12?style=for-the-badge)

---

<!-- DEPLOYMENT -->
![Joblib](https://img.shields.io/badge/Model%20Export-Joblib%20Serialized-2980B9?style=for-the-badge)
![Production](https://img.shields.io/badge/Status-Production%20Ready-27AE60?style=for-the-badge)

---

---

##  Project Overview

Customer churn prediction is one of the most important applications of machine learning in the telecom industry. Telecom companies lose significant revenue when customers discontinue services, and retaining existing customers is substantially cheaper than acquiring new ones.

This project builds a complete **industry-style machine learning pipeline** capable of predicting customer churn using customer demographics, billing information, and subscribed services.

The system was designed with a strong focus on:
- production-ready preprocessing,
- handling class imbalance,
- recall optimization,
- explainability,
- business-oriented evaluation.

---

# Business Problem

The primary objective is to identify customers who are likely to churn before they leave the company.

This allows businesses to:
- launch targeted retention campaigns,
- reduce customer loss,
- improve customer satisfaction,
- increase long-term revenue.

---

#  Why Churn Prediction is Challenging

Customer churn datasets are naturally **imbalanced**.

Most customers:
- stay with the company,
- while only a smaller percentage churn.

This creates a major challenge:

A model can achieve very high accuracy simply by predicting:

> “Most customers will not churn.”

However, such a model becomes useless from a business perspective because it fails to identify actual churners.

---

#  Why Recall is More Important than Accuracy

In this project, the primary optimization metric is:

#  Recall for Churn Customers

Recall measures:

> how many actual churn customers were correctly identified.

This is critical because:

## False Negative = Lost Customer

If the model fails to detect a churner:
- the customer leaves,
- revenue is lost,
- retention opportunity disappears.

Therefore:

✔ maximizing churn recall is more important than maximizing raw accuracy.

---

#  Dataset

Dataset Used:

## Telco Customer Churn Dataset

The dataset contains:
- demographic information,
- account information,
- billing behavior,
- subscribed services,
- churn labels.

---

#  Project Architecture

```text
Raw Data
   ↓
Data Cleaning
   ↓
Feature Engineering
   ↓
Preprocessing Pipeline
   ↓
Model Training
   ↓
Threshold Optimization
   ↓
Evaluation & Explainability
   ↓
Model Export (Joblib)
```

---

#  Data Preprocessing

- Missing value handling
- Scaling
- One-hot encoding
- Pipeline API (ColumnTransformer)

---

#  Models Used

- Logistic Regression  
- Random Forest  
- XGBoost (Best Model)

---

#  Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- ROC Curve
- Confusion Matrix

---

#  Final Results

| Model | Accuracy | Churn Recall |
|---|---|---|
| Logistic Regression | 74% | 79% |
| Random Forest | 78% | 68% |
| XGBoost | 75% |  80% |

---

#  Best Model

## XGBoost

Best performance for churn detection due to highest recall.

---

#  Model Export (PRODUCTION READY)

The final trained machine learning pipeline is saved using **Joblib** for real-world deployment.

###  Why Joblib is Important:
- Saves full ML pipeline (preprocessing + model)
- Enables reuse without retraining
- Used in production systems
- Supports deployment in APIs / apps

---

##  Save Model

```python
import joblib

joblib.dump(xgb_pipeline, "customer_churn_pipline/models/churn_pipeline.pkl")
```

---

##  Load Model (For Prediction)

```python
import joblib

model = joblib.load("customer_churn_pipline/models/churn_pipeline.pkl")

predictions = model.predict(X_test)
```

---

#  Visualizations Included

- Confusion Matrix  
- ROC Curve  
- Precision-Recall Curve  
- Feature Importance  

---

#  Key Business Insights

- Contract type strongly impacts churn
- Higher monthly charges increase churn risk
- New customers are more likely to churn

---

#  Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib  
- Joblib  

---

#  Production-Level Features

✔ End-to-end ML pipeline  
✔ Reusable preprocessing  
✔ Model serialization (Joblib)  
✔ Threshold tuning  
✔ Business-focused evaluation  

---

# Author

**Name:** Malik Muhammad Mudassir Iqbal

**Role:** Building real world production grade intelligent systems, Machine Learning Engineering

**Project:** End-to-End Customer Churn Prediction System  

---

 This project was built as part of an ML learning portfolio focused on:
- real-world machine learning pipelines  
- production-ready model deployment practices  
- business-oriented analytics  

---
 


#  Conclusion

This project demonstrates a complete machine learning system for customer churn prediction using production-grade practices.

The final model is:
- accurate enough for real-world use,
- optimized for recall,
- fully deployable using joblib pipeline serialization.