# 🏦 Bank Loan Analysis Dashboard

[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)](https://github.com/anushri2511/Bank-Loan-Report-Dashboard/tree/619b12c1f5594f60115f0fcc57051dddc1ecb946/Power%20BI)

[![Tableau](https://img.shields.io/badge/Tableau-Visualization-blue?logo=tableau)](https://github.com/anushri2511/Bank-Loan-Report-Dashboard/tree/1ef76bcffa575bc044e4b1b2db16fd95c73d95a7/Tableau)

[![Python](https://img.shields.io/badge/Python-EDA-green?logo=python)](https://github.com/anushri2511/Bank-Loan-Report-Dashboard/tree/e856ddca2b5ec847ba6a2eec6968f731ac5f7a7c/Python)

[![SQL](https://img.shields.io/badge/SQL-Database-orange?logo=mysql)](https://github.com/anushri2511/Bank-Loan-Report-Dashboard/tree/944e8dbb14e8b24455b852c2a979a31518c2a0fc/SQL)

An end-to-end **Bank Loan Analysis Project** developed using **Python, SQL, Power BI, and Tableau** to analyze loan applications, repayment trends, customer financial behavior, and loan risk performance.

This project transforms raw financial data into meaningful business insights through **data preprocessing, exploratory analysis, and interactive dashboards**.

---

# 📌 Project Objective

The primary objective of this project is to:

- Analyze bank loan applications and repayment trends
- Monitor good loans vs bad loans
- Track financial KPIs
- Identify customer borrowing behavior
- Visualize loan distribution across states and categories
- Support data-driven financial decision making

---

# 🛠️ Tech Stack

| Python | Data Cleaning & Analysis |
| Pandas | Data Manipulation |
| NumPy | Numerical Operations |
| Matplotlib / Seaborn | Data Visualization |
| SQL | Querying & Data Analysis |
| Power BI | Dashboard Development |
| Tableau | Data Visualization |
| DAX | KPI Calculations |
| Excel / CSV | Dataset Source |

---

# 📂 Project Workflow

Raw Dataset
     ↓
Data Cleaning using Python
     ↓
Exploratory Data Analysis (EDA)
     ↓
SQL Analysis & KPI Creation
     ↓
Power BI Dashboard
     ↓
Tableau Dashboard
     ↓
Business Insights & Reporting




# 🐍 Python Analysis

The Python notebook was used for:

- Data Cleaning
- Missing Value Handling
- Data Transformation
- Exploratory Data Analysis (EDA)
- KPI Validation
- Loan Trend Analysis


## Python Libraries Used

python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# 🗄️ SQL Analysis

SQL was used to perform data querying, KPI extraction, and business analysis on the bank loan dataset before visualization in Power BI and Tableau.

## SQL Operations Performed

- Data Filtering
- Aggregations & Grouping
- KPI Calculations
- Loan Status Analysis
- Monthly Trend Analysis
- Good Loan vs Bad Loan Analysis
- State-wise Loan Distribution
- Interest Rate Analysis

---

## Sample SQL Queries

### Total Loan Applications


SELECT COUNT(id) AS Total_Loan_Applications
FROM bank_loan_data;


### Total Funded Amount

SELECT SUM(loan_amount) AS Total_Funded_Amount
FROM bank_loan_data;


### Good Loan Percentage


SELECT 
    (COUNT(CASE WHEN loan_status = 'Fully Paid' THEN id END) * 100.0) 
    / COUNT(id) AS Good_Loan_Percentage
FROM bank_loan_data;


### Bad Loan Percentage


SELECT 
    (COUNT(CASE WHEN loan_status = 'Charged Off' THEN id END) * 100.0) 
    / COUNT(id) AS Bad_Loan_Percentage
FROM bank_loan_data;


### Monthly Loan Applications Trend

SELECT 
    MONTH(issue_date) AS Month_Number,
    DATENAME(MONTH, issue_date) AS Month_Name,
    COUNT(id) AS Total_Applications
FROM bank_loan_data
GROUP BY MONTH(issue_date), DATENAME(MONTH, issue_date)
ORDER BY Month_Number;

## SQL Insights Generated

✔️ Identified high-risk loan categories  
✔️ Calculated funded vs received amounts  
✔️ Tracked monthly application growth  
✔️ Analyzed repayment trends  
✔️ Compared good loans and charged-off loans  
✔️ Evaluated state-wise loan performance  


# 📊 Dashboard Pages

# 1️⃣ Summary Dashboard
# 📊 Dashboard Preview


The Summary Dashboard provides a high-level overview of overall loan performance.

### KPIs Included

- Total Loan Applications
- Total Funded Amount
- Total Amount Received
- Average Interest Rate
- Average DTI

### Additional Insights

- Good Loan Percentage
- Bad Loan Percentage
- Loan Status Analysis
- Month-to-Date (MTD) Metrics
- Month-over-Month (MoM) Growth

---

# 2️⃣ Overview Dashboard


The Overview Dashboard focuses on trends and distribution analysis.

### Visual Analysis

- Monthly Loan Trends
- State-wise Loan Distribution
- Loan Term Distribution
- Employee Length Analysis
- Loan Purpose Breakdown
- Home Ownership Analysis

### Visuals Used

- Line Charts
- Map Charts
- Donut Charts
- Treemaps
- Bar Charts

---

# 3️⃣ Details Dashboard


The Details Dashboard provides granular loan-level analysis.

### Information Included

- Loan ID
- Loan Purpose
- Home Ownership
- Grade & Sub-grade
- Loan Amount
- Interest Rate
- Installment Amount
- Amount Received

### Features

- Interactive Filters
- Dynamic Slicers
- Drill-through Analysis
- Detailed Loan Records

---

# 📈 Key Business Insights

✔️ Majority of loans are categorized as good loans  
✔️ Debt consolidation is one of the most common loan purposes  
✔️ Certain states contribute significantly to total loan applications  
✔️ Customers with longer employment history tend to have better repayment performance  
✔️ Fully paid loans contribute most to total amount received  
✔️ High DTI ratio is associated with higher loan risk  

---

# 🔍 Key KPIs

| KPI | Description |
|------|-------------|
| Total Loan Applications | Total number of loan applications |
| Total Funded Amount | Total sanctioned loan amount |
| Total Amount Received | Amount repaid by customers |
| Average Interest Rate | Average loan interest rate |
| Average DTI | Average debt-to-income ratio |
| Good Loan % | Percentage of fully paid loans |
| Bad Loan % | Percentage of charged-off loans |

---

# 📸 Dashboard Screenshots

## 🔹 Power BI Dashboard

### Summary Page
https://github.com/anushri2511/Bank-Loan-Report-Dashboard/blob/d6ebdab2d0a4dd809038fa80254a32003249922f/Power%20BI/Screenshot%202026-05-24%20000130.png
- Loan KPIs
- Good vs Bad Loan Analysis
- Loan Status Metrics

### Overview Page
https://github.com/anushri2511/Bank-Loan-Report-Dashboard/blob/870cebbc0bdddf8de3f9f2fa602b42eaa89238f6/Power%20BI/Screenshot%202026-05-24%20000135.png
- Loan Trends
- State-wise Analysis
- Purpose & Home Ownership Insights

### Details Page
https://github.com/anushri2511/Bank-Loan-Report-Dashboard/blob/870cebbc0bdddf8de3f9f2fa602b42eaa89238f6/Power%20BI/Screenshot%202026-05-24%20000139.png
- Detailed Loan Records
- Interactive Filtering

---

## 🔹 Tableau Dashboard

### Summary Dashboard
https://github.com/anushri2511/Bank-Loan-Report-Dashboard/blob/c6b0bec7f1fd3a302fcee020cd6207a329a26095/Tableau/Screenshot%202026-05-24%20000115.png
- KPI Monitoring
- Loan Status Analysis

### Overview Dashboard
https://github.com/anushri2511/Bank-Loan-Report-Dashboard/blob/c6b0bec7f1fd3a302fcee020cd6207a329a26095/Tableau/Screenshot%202026-05-24%20000119.png
- Trend Analysis
- Geographic Visualization
- Loan Category Distribution

### Details Dashboard
https://github.com/anushri2511/Bank-Loan-Report-Dashboard/blob/c6b0bec7f1fd3a302fcee020cd6207a329a26095/Tableau/Screenshot%202026-05-24%20000123.png
- Detailed Loan-Level Analysis
- Dynamic Filters

---



# 🎯 Project Highlights

- Built fully interactive dashboards
- Created professional dark-themed UI
- Used DAX measures for KPI calculations
- Performed EDA using Python
- Implemented dynamic filtering & drill-through
- Combined Power BI + Tableau + Python in one project
- Generated business insights from raw financial data

---

# 📚 Learning Outcomes

Through this project, I learned:

- Data Cleaning using Python
- Exploratory Data Analysis (EDA)
- Financial KPI Analysis
- Dashboard Designing
- Data Storytelling
- DAX Calculations
- Interactive Data Visualization
- Business Insight Generation

---

# 🚀 Future Improvements

- Predictive Loan Default Analysis
- Machine Learning Integration
- Risk Scoring Model
- Customer Segmentation
- Real-time Data Integration
- Automated Reporting

---

# 👨‍💻 Author

## Anushri Singh


Aspiring Data Analyst | CAT Aspirant

---

# 📬 Contact

- LinkedIn: (https://www.linkedin.com/in/anushri-singh-2578323a2/)
- Email: anushrisingh584@gmail.com

---

# ⭐ If you liked this project, don't forget to star the repository!
