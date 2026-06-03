# 🏆 Employee Promotion Forecasting

Predicting which employees are likely to be promoted using machine learning — built to support fairer, more data-driven HR decisions.

---

## 📌 Project Overview

In large organizations, identifying the right candidates for promotion is a critical and often subjective process. This project builds a classification model trained on real HR performance data to **forecast employee promotion eligibility** based on measurable factors such as training scores, performance ratings, awards, and tenure.

The goal is to give HR teams an objective, data-backed tool to shortlist candidates — not to replace human judgment, but to complement it.

---

## 📂 Dataset

| Property | Detail |
|---|---|
| **Source** | HR Analytics Dataset |
| **Records** | 54,808 employees |
| **Features** | 13 (department, education, gender, training score, rating, tenure, etc.) |
| **Target** | `is_promoted` (binary: 0 = Not Promoted, 1 = Promoted) |
| **Class imbalance** | ~8.7% promoted — handled using SMOTE |

---

## 🔍 Key EDA Findings

- **Awards won** is the strongest predictor — employees who won awards had a **44% promotion rate** vs only **7.7%** for those who didn't
- **Technology** department had the highest promotion rate (~10.8%), followed by Procurement and Analytics
- **Master's degree holders** are promoted at a slightly higher rate (9.9%) than Bachelor's holders (8.0%)
- Employees with **fewer but more impactful trainings** tend to get promoted more
- **Referred employees** show a higher promotion rate (12%) than those from other recruitment channels

---

## ⚙️ Methodology

```
Raw Data → EDA → Missing Value Handling → Outlier Removal
→ Encoding → Train/Test Split → SMOTE → Feature Scaling
→ Model Training → Evaluation → Feature Importance → Insights
```

### Models Trained
| Model | Notes |
|---|---|
| Logistic Regression | Baseline linear model |
| Random Forest | Ensemble tree-based model |
| XGBoost | Gradient boosting — best overall performance |

### Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- **AUC-ROC** — primary metric due to class imbalance
- Confusion matrices for all three models

---

## 📊 Results

| Model | Accuracy | F1-Score | AUC-ROC |
|---|---|---|---|
| Logistic Regression | — | — | — |
| Random Forest | — | — | — |
| XGBoost | — | — | — |

> ℹ️ Run the notebook to populate the results table with actual scores.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-lightgrey)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-Boosting-green)
![Plotly](https://img.shields.io/badge/Plotly-Visualization-purple)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-teal)
![Imbalanced-learn](https://img.shields.io/badge/Imbalanced--learn-SMOTE-red)

---

## 🚀 How to Run

1. Clone the repository
```bash
git clone https://github.com/salmaaamuhammed111/employee-promotion-forecasting.git
cd employee-promotion-forecasting
```

2. Install dependencies
```bash
pip install pandas numpy scikit-learn xgboost imbalanced-learn plotly seaborn matplotlib datasist
```

3. Open the notebook
```bash
jupyter notebook employee_promotion.ipynb
```

---

## 📁 Repository Structure

```
├── employee_promotion.ipynb   # Main analysis notebook
├── employee_promotion.csv     # Dataset
└── README.md                  # Project documentation
```

---

## 💡 Business Recommendation

> HR teams should prioritize candidates with high `avg_training_score`, strong `previous_year_rating`, and `awards_won` as the top predictors of promotion readiness. This model can serve as an objective shortlisting tool to reduce bias and support more transparent talent development decisions.

---

## 👩‍💻 Author

**Salma Mohamed** — Data Analyst  
📧 Salmaaamuhammed11@gmail.com  
🔗 [GitHub Profile](https://github.com/salmaaamuhammed111)
