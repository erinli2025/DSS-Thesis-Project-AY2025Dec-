For feature_df.csv, please use:https://drive.google.com/file/d/17BUrMVZbdVldUCD0XywkESfPdVw7SCoS/view?usp=sharing this link to download the file. 
# Supply Chain Order Delay Risk Prediction

MSc Thesis — Data Science and Society, Tilburg University (2025)

## Overview
This thesis compares three machine learning models — Logistic Regression, 
XGBoost, and Explainable Boosting Machine (EBM) — for predicting order delay 
risk in supply chains, with a focus on balancing predictive accuracy with 
model interpretability.

## Key Findings
- All three models achieved high predictive accuracy (>97%) on the DataCo 
  Supply Chain dataset (~180,000 orders)
- EBM matched XGBoost's state-of-the-art performance while remaining fully 
  transparent and producing the most balanced error distribution
- Core delay drivers identified: Shipping Mode, Order Processing Time, 
  and Order Status
- Systematic errors concentrated in same-day shipments, Pacific Asia orders, 
  low-profit transactions, and orders in transitional states (PENDING, 
  PROCESSING)

## Methods
- Feature engineering: geolocation (Nominatim API), temporal features, 
  leakage removal
- Models: Logistic Regression (baseline), XGBoost, EBM (InterpretML)
- Interpretability: SHAP (LR & XGBoost), EBM built-in feature importance
- Error analysis: Venn diagrams, t-SNE projection, t-tests

## Tools
Python · scikit-learn · XGBoost · InterpretML · SHAP · pandas · matplotlib
