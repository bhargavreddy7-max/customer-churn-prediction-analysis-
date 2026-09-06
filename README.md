# Customer Churn Prediction Analysis

## Overview
An exploratory data analysis project examining subscription customer data to uncover behavioral patterns and factors most associated with customer churn.

## Objective
Subscription businesses lose revenue when customers churn, often without a clear early signal. This project analyzed customer behavior data to identify which patterns most strongly predict churn, so retention efforts can be targeted before customers leave.

## Dataset
[Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (Kaggle) — 7,043 customer records including tenure, contract type, billing information, and churn status.

## Tools & Technologies
- **Microsoft Excel** — data cleaning, formula-based feature engineering, Pivot Table analysis, and charting

## Approach
1. **Data Cleaning** — Identified 11 rows with blank `TotalCharges` values, confirmed they corresponded to brand-new customers (tenure = 0), and replaced them with 0.
2. **Feature Engineering** — Created a `NewCustomer` flag using the formula `=IF(tenure<=1,"Yes","No")` to segment customers by how new they are.
3. **Pivot Table Analysis** — Built a Pivot Table comparing churn counts between new and established customers to calculate churn rate by segment.
4. **Visualization** — Created a bar chart comparing churn rate between the two segments.

## Key Findings
- Using a Pivot Table to segment customers by tenure, I compared churn rates between new customers (tenure ≤ 1 month) and established customers (tenure > 1 month).
- **New customers churned at a rate of 60.9%**, compared to **23.2%** for established customers — nearly **2.6x higher**, confirming that the first month is a critical risk window for customer retention.

| Segment | Total Customers | Churned | Churn Rate |
|---|---|---|---|
| Established Customers (tenure > 1 month) | 6,419 | 1,489 | 23.2% |
| New Customers (tenure ≤ 1 month) | 624 | 380 | 60.9% |

## Business Impact
- Recommended that the business prioritize onboarding and early engagement (e.g., welcome check-ins, proactive support outreach) specifically for customers in their first month, to reduce early churn and improve retention in the highest-risk window.

## Skills Demonstrated
Data cleaning · Formula-based feature engineering · Pivot Table analysis · Data visualization · Actionable business insight generation
