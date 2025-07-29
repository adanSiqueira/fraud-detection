# Credit Card Fraud Detection with Explainable AI

This project aims to build a **fraud detection system** for credit card transactions using **Machine Learning** techniques and **Explainable AI (XAI)** to ensure interpretability of the results — a crucial requirement in financial applications.

---

## Project Objectives

- ✅ Detect suspicious transactions in real-time
- ✅ Handle severe class imbalance (fraud is rare)
- ✅ Explain why a transaction was flagged as fraud (SHAP)
- ✅ Deliver a **robust, interpretable, and deployable model**

---

## Dataset Used

**[Credit Card Fraud Detection (Kaggle)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)**

- European credit card transactions
- 284,807 total transactions
- Only **492 fraud cases (0.172%)**
- Anonymized PCA-transformed features: V1 to V28
- Includes `Amount`, `Time`, and `Class` (fraud = 1)

---

## Project Pipeline

1. **Data Ingestion**
   - Load, check, clean, and sample the data

2. **Exploratory Data Analysis (EDA)**
   - Feature distribution, class imbalance
   - Correlation analysis, outlier visualization

3. **Class Imbalance Handling**
   - Undersampling + StratifiedKFold
   - Alternatives: SMOTE, Class Weights

4. **Modeling**
   - Models: Logistic Regression, Random Forest, XGBoost
   - Evaluation: AUC-ROC, Recall, Precision, F1-score

5. **Explainable AI**
   - SHAP for global and local explainability
   - Visualizations: Summary plot, Force plot

6. **Deployment**
   - Streamlit interface to input new transactions
   - Real-time prediction and explanation

7. **Monitoring (Optional)**
   - Score distribution over time
   - Optional integration with Evidently AI or MLflow

---

## 🗂️ Project Structure

```
fraud_detection_project/
|
├── data/                 # Raw and processed data
├── notebooks/            # Exploratory Jupyter Notebooks
├── src/                  # Core scripts
│   ├── ingestion.py      # Data loading and preprocessing
│   ├── train_model.py    # Model training and evaluation
│   ├── shap_analysis.py  # SHAP explainability
│   └── app.py            # Streamlit interface
|
├── requirements.txt      # Dependencies
└── README.md
```
