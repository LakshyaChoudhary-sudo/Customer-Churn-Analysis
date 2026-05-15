# 📊 Customer Churn Analysis — Telco Industry

**Analyst:** Lakshya Choudhary | BBA Business Analytics  
**Dataset:** IBM Telco Customer Churn (7,043 customers)  
**Tools:** Python · Scikit-learn · XGBoost · Power BI · Google Colab  

---

## 🏢 Business Problem

Customer churn — when a customer stops using a service — is one of the most costly challenges in the telecommunications industry. Acquiring a new customer costs **5–7× more** than retaining an existing one.

This project analyses 7,043 Telco customers to:
- Identify **why** customers are churning
- Build ML models to **predict** which customers will churn
- Deliver **actionable retention strategies** backed by data

---

## 📁 Project Structure

```
Customer-Churn-Analysis/
│
├── 📓 Notebooks/
│   ├── 01_EDA_Churn.ipynb                  # Exploratory data analysis
│   ├── 02_Logistic_Regression_Churn.ipynb  # Logistic regression model
│   ├── 03_Random_Forest_Churn.ipynb        # Random forest model (best)
│   ├── 04_XGBoost_Churn.ipynb             # XGBoost model
│   └── 05_Model_Comparison_Churn.ipynb    # All 3 models compared
│
├── 📊 Dashboard/
│   └── CHURN_VISUAL.pbix                  # Power BI dashboard (3 pages)
│
├── 📄 Report/
│   └── Churn_Analysis_Executive_Summary.docx
│
├── 📂 Data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│
└── README.md
```

---

## 🔍 Key Findings

| Finding | Insight |
|---|---|
| Overall churn rate | **26.5%** — 1 in 4 customers leaves |
| Highest risk contract | Month-to-month → **42.7% churn** |
| Critical retention window | **47% of churners leave in first 6 months** |
| Highest risk internet | Fiber optic → **41.9% churn** |
| Highest risk payment | Electronic check → **45% churn** |
| Revenue at risk | **$139K per month** lost to churn |

---

## 🤖 Machine Learning Models

| Model | Accuracy | Precision | Recall | F1 | AUC-ROC |
|---|---|---|---|---|---|
| Logistic Regression | 74.0% | 50.7% | 78.6% | 61.6% | 0.841 |
| **Random Forest** ⭐ | **76.9%** | **54.9%** | **74.1%** | **63.0%** | **0.842** |
| XGBoost | 76.1% | 53.6% | 74.1% | 62.2% | 0.835 |

**Best Model: Random Forest** — selected based on highest AUC-ROC (0.842)  
**Top predictors:** Tenure · Monthly Charges · Contract Type · Internet Service

---

## 📊 Power BI Dashboard

Three interactive pages:

**Page 1 — Executive Summary**
- KPI cards: Total customers, churn rate, revenue lost, high risk count
- Churn rate by contract type, tenure group, internet service
- Customer risk distribution donut chart

**Page 2 — At-Risk Customer List**
- Filterable table of all 7,043 customers with churn probability scores
- Filter by Risk Segment and Contract Type

**Page 3 — Business Insights**
- Monthly charges vs tenure scatter chart
- Revenue lost by tenure group
- Churn rate by payment method
- Key findings and recommendations

---

## 💡 Business Recommendations

**Immediate Actions**
- Contact all **1,997 High Risk** customers within 48 hours
- Offer 15–20% loyalty discount or service upgrade

**Short Term**
- Launch contract upgrade campaign for month-to-month customers
- Add retention incentive at month 3 and month 6

**Long Term**
- Investigate Fiber Optic dissatisfaction via NPS surveys
- Bundle TechSupport with Fiber Optic plans
- Incentivise auto-pay to reduce Electronic check usage

---

## 🚀 How to Run

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

### Steps
1. Clone this repository
2. Place `WA_Fn-UseC_-Telco-Customer-Churn.csv` in the `Data/` folder
3. Open Google Colab or Jupyter Notebook
4. Run notebooks in order: 01 → 02 → 03 → 04 → 05
5. Open `CHURN_VISUAL.pbix` in Power BI Desktop

### Google Colab Setup
```python
from google.colab import files
files.upload()  # Upload the CSV file

!pip install xgboost -q
```

---

## 📦 Dependencies

| Library | Version | Purpose |
|---|---|---|
| pandas | Latest | Data manipulation |
| numpy | Latest | Numerical operations |
| matplotlib | Latest | Visualisation |
| seaborn | Latest | Statistical plots |
| scikit-learn | Latest | ML models (LR, RF) |
| xgboost | Latest | XGBoost model |

---

## 📄 Dataset

**Source:** IBM Sample Dataset — Telco Customer Churn  
**Available on:** [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
**Rows:** 7,043 customers | **Columns:** 21 features | **Target:** Churn (Yes/No)

---

## 👤 Author

**Lakshya Choudhary**  
BBA Business Analytics | MBA Aspirant  
📧 lakshyachoudhary2104@gmail.com
🔗 www.linkedin.com/in/lakshya-choudhary-82776a24b

---

*This project was completed as part of a personal portfolio to demonstrate skills in data analysis, machine learning and business intelligence.*
