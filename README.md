# CQF Exam 3 (Jan 2025) - QQQ Uptrend Prediction

This repository contains my submission for **Exam 3** of the **CQF (Certificate in Quantitative Finance)** program, January 2025 batch.

## 🎯 Objective

Develop a machine learning model to **predict daily uptrends** in **QQQ**, an exchange-traded fund (ETF) tracking the **Nasdaq-100 Index**. The model uses a **binomial classification approach** based on **10 years of historical data (2015–2025)**.

## 🧠 Methodology

### 📌 Target Definition
- Defined the prediction target as **positive daily returns** (i.e., uptrend movement).

### 🛠️ Feature Engineering
- **Market-derived features** from QQQ trading data.
- **Sentiment features** extracted from news headlines using AI-based NLP.
- **Macroeconomic indicators**, including the **Federal Reserve interest rate**.

### 🧪 Feature Selection
Applied multiple strategies to reduce multicollinearity and select informative features:
- **Filter methods**: Variance Inflation Factor (VIF)
- **Wrapper methods**: Recursive Feature Elimination (RFE)
- **Embedded methods**: SHAP value analysis

### 🤖 Model Training & Evaluation
- Tested and tuned:
  - `XGBoost`
  - `AdaBoost`
  - `LightGBM`
- Evaluated model performance using classification metrics.
- Selected the best-performing model for final deployment.

### 🔁 Backtesting
- Conducted backtesting using the full 10-year pricing dataset to assess predictive robustness.

## ⚠️ Limitations

- **Uniform scaling**: All features were scaled using `StandardScaler`, without accounting for individual feature distributions.
- **Non-stationary features**: Indicators like `SMA` and `EMA` were included without proper detrending or leakage control, potentially introducing bias.

## 📂 Files Included

| File | Description |
|------|-------------|
| `Exam3_Jan2025 Original.pdf` | Official exam question |
| `LI_Report.pdf`              | Full written answer |
| `LI_Code.ipynb`              | Executable Jupyter notebook |
| `LI_Code.html`               | HTML export of the notebook |

---

Feel free to explore the code and report. Feedback and suggestions are welcome!
