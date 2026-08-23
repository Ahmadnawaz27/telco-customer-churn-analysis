# Telco Customer Churn Analysis

An interactive Tableau dashboard exploring what drives customer churn at a fictional telecom provider, and which customer segments are highest risk.

**[View the live interactive dashboard on Tableau Public](https://public.tableau.com/app/profile/ahmad.nawaz4425/viz/telco_churn_dashboard_17874404917060/TELCOCHURNDASHBOARD)**

![Dashboard preview](dashboard_preview.png)

## The question

What drives customer churn, and who's at risk?

## Key findings

- Month-to-month customers churn at roughly 4x the rate of two-year contract customers (42.7% vs 2.8%)
- Nearly half of all churn happens within a customer's first 12 months
- Customers on Electronic check payments churn at 45.3%, more than double every other payment method
- Fiber optic customers churn at over twice the rate of DSL customers
- The single biggest churn driver by volume is dissatisfaction with support staff attitude, ahead of any competitor-related reason
- The highest-risk segment overall: new customers (0-12 months tenure) paying high monthly charges ($70+)

## Dataset

[IBM Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn), 7,043 customers, 33 original fields covering account details, services subscribed, billing, and churn outcome/reason.

## Tools

- **Python (Pandas)** for data cleaning: handled nulls, dropped non-analytical columns, engineered a tenure-band feature
- **Tableau Public** for the dashboard: 8 visualizations including stacked bar charts, a line chart, a two-dimensional heat map, and a grouped pie chart

## Approach

1. Cleaned and prepared the raw dataset in Python
2. Explored churn rate across contract type, internet service, payment method, and tenure
3. Built a heat map cross-referencing tenure and monthly charges to find the highest-risk combination
4. Grouped 20+ free-text churn reasons into three strategic categories (competitor-driven, service problems, pricing) to separate what's controllable from what isn't
5. Designed the dashboard around a consistent visual language (single accent color, card-based layout, one color meaning "churned" throughout) rather than default chart styling

## Files in this repo

- `telco_churn_clean.csv` — cleaned dataset used for the dashboard
- `data_cleaning.py` — Python script used to clean and prepare the raw data
- `dashboard_preview.png` — static preview image of the dashboard