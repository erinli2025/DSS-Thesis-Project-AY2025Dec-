For feature_df.csv, please use:https://drive.google.com/file/d/17BUrMVZbdVldUCD0XywkESfPdVw7SCoS/view?usp=sharing this link to download the file. 
# Supply Chain Order Delay Risk Prediction

MSc Thesis — Data Science and Society, Tilburg University (2025)

## Overview
This thesis compares three machine learning models — Logistic Regression, 
XGBoost, and Explainable Boosting Machine (EBM) — for predicting order delay 
risk in supply chains, with a focus on balancing predictive accuracy with 
model interpretability.

## Key Findings

**Model Performance**

| Model | AUC-ROC | Accuracy | F1 (Macro) |
|-------|---------|----------|------------|
| Logistic Regression | 0.9988 | 0.9761 | 0.98 |
| XGBoost | 0.9997 | 0.9907 | 0.99 |
| EBM | 0.9997 | 0.9917 | 0.99 |

**Feature Importance (EBM)**
<img width="740" height="671" alt="image" src="https://github.com/user-attachments/assets/882f0724-2047-404a-9731-218179095089" />


**Error Analysis — Which orders are hardest to predict?**
<img width="707" height="487" alt="image" src="https://github.com/user-attachments/assets/c5422de7-5924-4f3e-83ff-5c74a1a06121" />
<img width="889" height="647" alt="image" src="https://github.com/user-attachments/assets/497a4d4e-da80-4102-bd78-126091289a78" />


- EBM achieved the most balanced error distribution (120 FN vs 106 FP)
- All models struggle with the same hard cases: Same Day shipments, 
  Pacific Asia orders, low-profit transactions, PENDING/PROCESSING states
- Core delay drivers: Shipping Mode, Order Processing Time, Order Status




## Methods
- Feature engineering: geolocation (Nominatim API), temporal features, 
  leakage removal
- Models: Logistic Regression (baseline), XGBoost, EBM (InterpretML)
- Interpretability: SHAP (LR & XGBoost), EBM built-in feature importance
- Error analysis: Venn diagrams, t-SNE projection, t-tests

## Tools
Python · scikit-learn · XGBoost · InterpretML · SHAP · pandas · matplotlib
