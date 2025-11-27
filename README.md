# Credit-card-spending-Analysis

American Express Style Credit Card Spending and Risk Analysis Dashboard
# American Express Style Credit Card Spending & Risk Analysis

This project analyzes customer credit card spending patterns and identifies credit risk segments using Power BI. The dataset includes customer demographics, credit scores, and transaction history. The dashboard provides insights similar to what financial companies like American Express use for decision-making.

---

📊 Project Overview

The project consists of two datasets:
1. **credit_customers.csv** – customer demographics, income, city, credit score  
2. **credit_transactions.csv** – spending amount, merchant category, date, and payment method

The dashboard includes:
- Total Spend
- Average Monthly Spend
- Total Transactions
- Spending by Merchant Category
- Monthly Spending Trends
- Credit Score Distribution
- High-Risk Customer Identification
- Spend by Risk Group (Low, Medium, High)

---

🛠 Tools & Technologies Used
- **Power BI** – Dashboard & Data Visualization  
- **Excel/CSV** – Data Storage  
- **DAX** – Measures  
- **Data Cleaning Techniques**

---

🧮 Key DAX Measures
Total Spend = SUM('credit_transactions'[Amount])

Average Monthly Spend =
DIVIDE(
SUM('credit_transactions'[Amount]),
DISTINCTCOUNT('credit_transactions'[Month])
)

High Risk Customers =
COUNTROWS(
FILTER('credit_customers', 'credit_customers'[Credit_Score] < 600)
)

Score Group =
IF(
'credit_customers'[Credit_Score] < 600, "High Risk",
IF('credit_customers'[Credit_Score] < 700, "Medium Risk", "Low Risk")
)


---

📈 Dashboard Insights

- Customers aged 25–35 contribute the highest spending activity.
- Online Services and Shopping are the top spending categories.
- About 18% of customers fall under **High Risk** (Credit Score < 600).
- High-risk customers spend ~22% more than low-risk customers.
- Bangalore and Mumbai show the highest spending volume.

---

📂 Files Included

- `credit_customers.csv`
- `credit_transactions.csv`
- `credit-card-analysis.pbix` (Power BI file)
- `README.md`

---

👨‍💻 Author  
JERRY JAMES  
MCA Student | Data Analytics Enthusiast  

