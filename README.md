# 💳 AI-Powered Fraud Detection System

An end-to-end Machine Learning project that detects suspicious financial transactions using classification models, feature engineering, and a real-time Streamlit dashboard.

---


##  Dataset Link:[https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud]
---

## 🚀 Project Overview

This project builds a fraud detection system that classifies transactions as:

- ✅ Non-Fraud (Legitimate)
- 🚨 Fraud (Suspicious Activity)

It uses machine learning models trained on highly imbalanced financial transaction data and selects the best model based on evaluation metrics.

---

## 🎯 Objectives

- Build a fraud detection ML system
- Handle imbalanced dataset using SMOTE
- Train multiple models:
  - Logistic Regression
  - Random Forest
  - XGBoost
- Evaluate using:
  - Precision
  - Recall
  - F1-Score
  - ROC-AUC
  - Average Precision (PR-AUC)
- Deploy using Streamlit dashboard
- Enable real-time predictions

---

## 📊 Dataset Information

The dataset contains credit card transactions:

- `Time` → Seconds since first transaction  
- `Amount` → Transaction value  
- `V1–V28` → PCA-transformed anonymized features  
- `Class` → Target variable  
  - `0` → Non-Fraud  
  - `1` → Fraud  

⚠️ Note: V1–V28 are PCA components and not human-interpretable.

---

## ⚙️ Tech Stack

- Python 🐍
- Pandas & NumPy
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Matplotlib
- Streamlit
- Joblib

---

## 🧠 Machine Learning Workflow

### 1. Data Preprocessing
- Handling missing values
- Feature scaling using `RobustScaler`
- Handling imbalance using **SMOTE**

---

### 2. Feature Engineering
Created new features:

- `log_amount`
- `amount_to_mean`
- `is_high_amount`
- `is_night`
- `hour` extracted from Time

---

### 3. Model Training
Models used:

- Logistic Regression
- Random Forest
- XGBoost

---

### 4. Model Evaluation
Metrics used:

- ROC-AUC Score
- Average Precision Score
- Confusion Matrix
- Precision-Recall Curve

---

### 5. Model Selection
Best model is selected based on **Average Precision (PR-AUC)**.

---

## 🏆 Model Performance

| Model               | Average Precision | ROC-AUC |
|--------------------|------------------|--------|
| Logistic Regression | 0.73             | 0.97   |
| Random Forest       | 0.87             | 0.97   |
| XGBoost             | 0.87             | 0.98   |


---

## 🚨 Fraud Flagging System

Transactions are flagged based on model probability threshold.

Output saved as:  flagged_transactions.csv


---

## 📈 Key Insights

- Fraud cases are extremely rare (highly imbalanced dataset)
- SMOTE improves minority class detection
- Tree-based models perform best (Random Forest, XGBoost)
- Precision-Recall metrics are more important than accuracy

---

## ⚠️ Limitations

- V1–V28 features are PCA-transformed (not interpretable)
- Requires retraining for real-time production systems
- No direct banking API integration yet

---

## 🚀 Future Improvements

- Real-time fraud API (Flask/FastAPI)
- SHAP explainability (why fraud was predicted)
- Live transaction monitoring dashboard
- Email/SMS fraud alert system
- Database integration (SQL/MongoDB)

---

## 👨‍💻 Author

**Tooba Azizullah**  
Data Science & AI Enthusiast  
Focus: Machine Learning, Fraud Detection, AI Systems

---

## ⭐ Support

If you like this project, please ⭐ the repository on GitHub!
