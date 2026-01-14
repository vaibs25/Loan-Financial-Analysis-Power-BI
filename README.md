# Loan-Financial-Analysis-Power-BI

📌 Project Overview

This project analyzes financial and customer data of a loan service provider to understand the customer base, loan portfolio performance, and financial risk exposure.

Using Power BI, the project transforms raw financial data into insightful dashboards that help stakeholders:

Assess customer demographics

Monitor loan distribution and performance

Identify financial risk and default patterns

The final solution consists of three interactive dashboard pages, each focusing on a critical business area.

🎯 Business Objectives

Understand customer demographics and credit behavior

Evaluate loan portfolio distribution and performance

Identify high-risk and default-prone customers

Support financial risk management decisions

Enable interactive analysis using slicers and filters

🛠️ Tools & Technologies

Power BI Desktop

Power Query – Data transformation

DAX – Measures & calculations

GitHub – Version control & documentation

📊 Dashboard Structure
📄 Page 1 – Customer Demographics

Page Name: Customer Demographics

🔢 KPI Cards

Total Customers

Average Age

Average Income

🎛️ Slicers

Income Buckets

Credit Score Buckets

📈 Visuals
1️⃣ Customer bifurcation with Gender

Type: Pie Chart

Legend: Gender

Values: Count of Customer ID

2️⃣ Customer bifurcation with Education Level

Type: Pie Chart

Legend: Education Level

Values: Count of Customer ID

3️⃣ Credit Score by Gender and Education Level

Type: Clustered Bar Chart

Y-Axis: Gender

X-Axis: Average Credit Score

Legend: Education Level

📌 Purpose:
Provides a demographic overview and credit profile distribution of customers.

📄 Page 2 – Loan Portfolio & Performance

Page Name: Loan Portfolio & Performance

🔢 KPI Cards

Total Loan Amount

Average Monthly Installment

🎯 Gauge Visual

Value: Average Interest Rate

Min: Minimum Interest Rate

Max: Maximum Interest Rate

🎛️ Slicers

Income Group

Credit Score Bucket

📈 Visuals
1️⃣ Loan Distribution by Type

Type: Pie Chart

Legend: Loan Type

Values: Count of Loan ID

2️⃣ Loans split by Type and Status

Type: 100% Stacked Column Chart

X-Axis: Loan Type

Y-Axis: Count of Loan ID

Legend: Status

3️⃣ Top 10 Active Loans

Type: Table

Columns: Name, Loan Amount, Loan Type

Filters:

Top 10 by Sum of Loan Amount

Status = Active

Label: Active

4️⃣ Top 10 Defaulted Loans

Type: Table

Columns: Name, Loan Amount, Loan Type

Filters:

Top 10 by Sum of Loan Amount

Status = Defaulted

Label: Defaulted

📌 Purpose:
Analyzes loan distribution, performance, and identifies high-value active and defaulted loans.

🔄 Data Transformation & Categorization
🏷️ Risk Category (Conditional Column)

Table: Customer_Details

Credit_Score < 580  → High Risk
Credit_Score < 670  → Moderate Risk
Credit_Score < 740  → Low Risk
Else               → Very Low Risk

📐 Measures Created (DAX)
🔴 Default Risk Measures

Defaulted_Loans
→ Count of loans with Status = "Defaulted"

Defaulted_Loan_Amount
→ Sum of Loan Amount for defaulted loans
(Currency format)

⚠️ High Risk Measures

High_Risk_Loans
→ Count of loans with Risk Category = "High Risk"

High_Risk_Loan_Amount
→ Sum of Loan Amount for High Risk loans
(Currency format)

📄 Page 3 – Financial Risk Analysis

Page Name: Financial Risk Analysis

🔢 KPI Cards

Defaulted Loans

Defaulted Loan Amount

High Risk Loans

High Risk Loan Amount

🎛️ Slicers

Income Group

Credit Score Bucket

📈 Visuals
1️⃣ Defaulted Loans & Amount

Type: Donut Chart

Legend: Employment

Values: Defaulted Loan Amount

Tooltips: Defaulted Loans

2️⃣ Default Risk Matrix

Type: Matrix

Rows: Income, Education Level

Values: Defaulted Loans, Defaulted Loan Amount

3️⃣ High Risk Loan Amount

Type: Donut Chart

Legend: Employment

Values: High Risk Loan Amount

Tooltips: High Risk Loans

4️⃣ High Risk Matrix

Type: Matrix

Rows: Income, Education Level

Values: High Risk Loans, High Risk Loan Amount

5️⃣ Credit Score vs Customers

Type: Stacked Column Chart

X-Axis: Credit Score Buckets

Y-Axis: Count of Customer ID

Legend: Employment Status

📌 Purpose:
Provides deep insights into financial risk exposure, default behavior, and credit risk patterns.

🚀 Key Insights Enabled

Identification of high-risk customer segments

Analysis of defaulted loan concentration

Understanding of income, education, and employment impact on risk

Visibility into loan portfolio health

📁 Project Files

📊 Loan_Financial_Analysis.pbix – Power BI dashboard

📄 README.md – Project documentation

🧠 Skills Demonstrated

Power BI Data Modeling

DAX Measures & Conditional Columns

Financial Risk Analysis

KPI Design & Dashboard Layout

Business-Oriented Data Visualization
