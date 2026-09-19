
# Supply Chain Order Delay Risk Prediction


> 📊 **[Interactive Dashboard (Power BI)](https://app.powerbi.com/view?r=eyJrIjoiOWMyMWMyZTgtZWFlYS00OTRiLTg3NGQtODUxMDgyNjZmNTlhIiwidCI6IjU2M2FmYzRkLWQxZTAtNDRhMy1iYjc0LWMxZTkzN2RlMmVjMyJ9)**　｜　🖼 **[Full Snapshot (PDF)](https://drive.google.com/file/d/14sVRkSL9MOD32upzCbkbCOsrx95OvJgp/view)**　｜　🔍 **[Project Overview Page]([你的GitHub Pages链接](https://erinli2025.github.io/thesis_portfolio/))**

Comparing Logistic Regression, XGBoost, and Explainable Boosting Machine (EBM) for supply chain order delay prediction — with a focus on balancing accuracy and interpretability.

## Key Results

| Model | AUC-ROC | Accuracy | F1 (Macro) | FN:FP Ratio |
|---|---|---|---|---|
| Logistic Regression | 0.9989 | 97.6% | 0.98 | 0.14 ⚠ |
| XGBoost | 0.9997 | 99.1% | 0.99 | 0.64 |
| **EBM** | **0.9998** | **99.3%** | **0.99** | **0.88 ✓** |

EBM matches black-box accuracy while providing full inherent interpretability and the most balanced error distribution.

## Setup

```bash
pip install -r requirements.txt  # or see library list in notebook
```

**Dataset:** Download `feature_df.csv` from [Google Drive](https://drive.google.com/file/d/17BUrMVZbdVldUCD0XywkESfPdVw7SCoS/view?usp=sharing) and place it in the project root.

## How to Run

Open `DSS-Code.ipynb` and run all cells in order. The notebook covers data preprocessing, model training, evaluation, and error analysis end-to-end.

## Methods

- **Feature engineering:** geolocation via Nominatim API, temporal decomposition, leakage removal, OOF target encoding
- **Models:** Logistic Regression (baseline) · XGBoost · EBM (InterpretML)
- **Interpretability:** SHAP for LR & XGBoost · EBM built-in feature contribution curves
- **Error analysis:** Venn diagrams · t-SNE projection · t-tests on misclassified samples

## Tools

Python 3.10 · scikit-learn · XGBoost · InterpretML · SHAP · pandas · matplotlib · geopy
