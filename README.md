# 💳 Mitron Bank — Credit Card Launch: Customer Insights

A data analysis project simulating a real-world consulting engagement: analyzing customer spending behavior to guide a new credit card product launch for a fictional bank, **Mitron Bank**.

![Status](https://img.shields.io/badge/status-complete-brightgreen)
![Python](https://img.shields.io/badge/Python-Pandas-blue)
![Power BI](https://img.shields.io/badge/Dashboard-Power%20BI-yellow)

---

## 📌 Project Background

Mitron Bank, a legacy financial institution, wants to launch a new line of credit cards. Before committing to a full-scale engagement, the bank's strategy director requested a **pilot analysis** on a sample of 4,000 customers to evaluate whether the proposed analytics approach could deliver actionable insights.

Acting as the analyst on this pilot, the goal was to:
1. Understand customer demographics and spending behavior
2. Identify the customer segments most likely to adopt a new credit card
3. Recommend specific card features backed by data
4. Deliver findings via a dashboard suitable for a non-technical executive audience

---

## 🗂️ Dataset

| File | Description | Rows |
|---|---|---|
| `dim_customers.csv` | Customer demographics (age group, city, occupation, gender, marital status, income) | 4,000 |
| `fact_spends.csv` | Monthly transaction-level spend by category and payment type (May–Oct) | 864,000 |

**Data quality note:** During analysis, 5 discrepancies were identified between the raw data and the provided metadata documentation (inconsistent column naming, city label formatting, and value casing). These were standardized before analysis and documented in the final presentation, as flagged in the project brief.

---

## 🛠️ Tools & Tech Stack

- **Python** (Pandas, Matplotlib, Seaborn) — data cleaning, exploratory analysis, metric engineering
- **Jupyter Notebook** — analysis documentation and reproducibility
- **Power BI** — interactive dashboard for stakeholder-facing delivery
- **DAX** — custom measures for KPI cards and aggregations

---

## 🔑 Key Metric: Income Utilisation %

To evaluate credit-readiness, a custom metric was engineered:

```
Income Utilisation % = (Average Monthly Spend ÷ Average Monthly Income) × 100
```

This proved to be a far stronger signal of card-readiness than raw income alone.

---

## 📊 Key Findings

- **Income does not predict spending behavior.** Across occupation, city, and age cuts, the highest-earning segment was consistently *not* the one with the highest income utilisation. Business Owners had the highest average income (₹70,091) but the lowest utilisation (33.2%); the 45+ age group showed the same pattern (highest income, 35.1% utilisation — the lowest of any age group).
- **Best-fit segment:** Salaried IT Employees combine strong income (₹61,500 avg.) with the highest utilisation in the dataset (50.9%). Narrowing further, IT employees aged 25–45 in Mumbai and Delhi-NCR reach 52–61% utilisation with sufficient customer volume (~880 customers) to anchor a launch.
- **Spending is essentials-heavy:** Bills, Groceries, and Electronics account for ~51% of total spend — the natural categories for a rewards structure.
- **A youth anomaly:** The 21–24 age group is the only segment where Entertainment — not Bills — is the top spending category, suggesting demand for a distinct youth-oriented card.
- **Market readiness:** Credit Card is already the leading payment method by value (40.7%), ahead of UPI (26.5%), indicating strong existing comfort with card-based spending.

---

## 💡 Feature Recommendations

| Segment | Recommended Feature |
|---|---|
| Salaried IT Employees, 25–45, Mumbai/Delhi-NCR | Premium cashback card — Bills, Groceries & Electronics |
| 21–24 age group | Youth starter card — Entertainment & food-delivery cashback |
| Freelancers | Flexible-limit card — no fixed income requirement, EMI conversion |
| UPI-heavy spenders | RuPay-on-UPI integration |
| 45+ age group | Premium lifestyle card — travel & lounge benefits |

---

## 📈 Dashboard

An interactive 2-page Power BI dashboard was built for the Mitron Bank strategy team, featuring:
- KPI summary cards (customers, avg. income, avg. spend, avg. utilisation %)
- Demographic breakdowns (age, occupation, city, gender)
- Income utilisation analysis (bar charts, income-vs-utilisation scatter plot)
- Spending pattern visuals (category spend, payment type mix, category mix by age)
- A ranked, filterable table of highest-value customer segments
- Cross-filtering slicers (city, age group, occupation, gender)

> 📸 *Add dashboard screenshots here*

## 🙋 About This Project

This project was completed as part of the **Codebasics Resume Project Challenge**, simulating a real analytics consulting engagement.

**Author:** [Pooja]

**Connect:** [www.linkedin.com/in/pooja-singh-45913a24a] 
