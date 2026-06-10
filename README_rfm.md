# 👥 Customer Segmentation — RFM Analysis

> **A business-focused customer segmentation project using the RFM (Recency, Frequency, Monetary) framework on 2 years of online retail data — scoring and classifying customers into VIP, Potential Loyal, At-Risk, Can't Lose, and Lost segments with fully interactive Plotly visualizations.**

---

## 📌 Project Overview

Understanding *who* your customers are is the foundation of every successful marketing strategy. This project applies the industry-standard **RFM Analysis** framework to transform raw transaction data into a rich customer segmentation model — enabling businesses to personalize campaigns, reduce churn, and maximize customer lifetime value.

**Analyst:** Jawad Khan — Aspiring Data Scientist  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Jawad%20Khan-blue?logo=linkedin)](https://www.linkedin.com/in/jawad-khan-133755408)
[![GitHub](https://img.shields.io/badge/GitHub-jawad--khan710-black?logo=github)](https://github.com/jawad-khan710)

---

## 🎯 Business Problem

Companies struggle to answer critical CRM questions like:

- Who are the most valuable customers worth protecting?
- Which customers are quietly drifting toward churn?
- Where should marketing budgets be focused?
- How can campaigns be personalized per customer group?

This project answers all of these using a data-driven RFM scoring system.

---

## 📂 Project Structure

```
rfm-customer-segmentation/
│
├── RFM_Analysis.ipynb          # Full analysis notebook
├── online_retail_II.xlsx       # Transaction dataset (2009–2011)
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

> ⚠️ **Dataset Note:** Download from [Kaggle — Online Retail II Dataset](https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci) and place in the root folder.

---

## 🗃️ Dataset

Transactional records from a UK-based online retail store (2009–2011).

| Feature | Description |
|---------|-------------|
| `Invoice` | Transaction ID |
| `StockCode` | Product ID |
| `Description` | Product name |
| `Quantity` | Units purchased |
| `InvoiceDate` | Transaction date |
| `Price` | Unit price |
| `Customer ID` | Unique customer identifier |
| `Country` | Customer country |

**Engineered Feature:** `Total_Amount = Quantity × Price`

---

## 🔧 Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0-lightblue?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-1.26-orange?logo=numpy)
![Plotly](https://img.shields.io/badge/Plotly-5.0-lightblue?logo=plotly)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-teal)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

## 🔄 Project Workflow

```
Raw Transaction Data (online_retail_II.xlsx)
      ↓
1. Data Cleaning
   • Removed missing values (heatmap visualization)
   • Removed duplicate records
   • Created Total_Amount feature (Quantity × Price)
      ↓
2. RFM Feature Engineering
   • Reference Date = Last Invoice Date + 1 day
   • Recency  = Days since last purchase (lower = better)
   • Frequency = Total number of transactions
   • Monetary  = Total revenue generated
      ↓
3. RFM Scoring (Quartile-Based)
   • Each customer scored 1–4 on R, F, M
   • Recency: lower days → higher score
   • Frequency & Monetary: higher value → higher score
   • RFM Total Score = R + F + M (range: 3–12)
      ↓
4. Customer Segmentation
   ┌─────────────────────────────────────────────┐
   │ Score ≥ 9   → High Value                    │
   │ Score 5–8   → Mid Value                     │
   │ Score < 5   → Low Value                     │
   └─────────────────────────────────────────────┘
      ↓
5. Advanced Segment Labels
   ┌─────────────────────────────────────────────┐
   │ Score ≥ 9         → VIP / Loyal             │
   │ Score 6–8         → Potential Loyal         │
   │ Score = 5         → At-Risk Customer        │
   │ Score = 4         → Can't Lose              │
   │ Score ≤ 3         → Lost                    │
   └─────────────────────────────────────────────┘
      ↓
6. Interactive Visualizations (Plotly)
   • Bar chart: Customer count per segment
   • Treemap: Segment hierarchy by value
   • Boxplots: VIP R/F/M distributions
   • Grouped bar: Avg R, F, M scores per segment
   • Heatmap: RFM score correlation within VIP group
```

---

## 📊 Key Insights

| Insight | Detail |
|---------|--------|
| **VIP / Loyal customers** | ~1,700 customers — highest revenue contributors |
| **Mid Value customers** | ~1,900 customers — largest group, strong growth potential |
| **Low Value customers** | ~800 customers — at risk of leaving, need re-engagement |
| **Typical purchase cycle** | Most customers return within 0–150 days; some up to 350 days |
| **Bulk buyers** | Some VIP customers place orders of 5,000+ items — bulk/wholesale buyers |
| **Returns detected** | Negative monetary values identified — product return behavior captured |

---

## 🏪 Business Recommendations

| Segment | Strategy |
|---------|----------|
| **VIP / Loyal** | Loyalty programs, exclusive offers, premium service, early access |
| **Potential Loyal** | Personalized promotions, cross-selling, targeted email campaigns |
| **At-Risk** | Win-back campaigns, time-sensitive discounts, personalized outreach |
| **Can't Lose** | Immediate re-engagement offers, survey to understand dissatisfaction |
| **Lost** | Low-cost reactivation campaigns or remove from active marketing |

---

## 🚀 Future Improvements

- [ ] Add **Customer Lifetime Value (CLV)** prediction using ML
- [ ] Build a **Churn Prediction Model** targeting At-Risk customers
- [ ] Apply **K-Means Clustering** as an alternative segmentation method
- [ ] Create an interactive **RFM Dashboard** in Power BI or Streamlit
- [ ] Extend analysis with **country-level segmentation**

---

## ⚙️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/jawad-khan710/rfm-customer-segmentation.git
cd rfm-customer-segmentation

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download the dataset from Kaggle
# https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci
# Place online_retail_II.xlsx in the root folder

# 4. Launch the notebook
jupyter notebook RFM_Analysis.ipynb
```

---

## 📬 Connect with Me

> *This project is part of my Data Science & Machine Learning portfolio.*  
> *Open to feedback, collaboration, and opportunities!*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/jawad-khan-133755408)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/jawad-khan710)
