# Business-Data-Analysis

## Report Link:
https://app.powerbi.com/links/8eFGY8TWBG?ctid=5bcca112-41e4-4d5e-a805-c5ba21ed65b6&pbi_source=linkShare

## Project Overview

This project demonstrates the end-to-end development of a data analytics pipeline for business transactions. The process began with synthetic data creation in SQL Server (with intentional inconsistencies), followed by data cleaning & transformation, and finally building an interactive Power BI dashboard with DAX-driven KPIs.

The goal was to simulate real-world data quality issues and showcase how structured data pipelines and BI tools can convert raw data into actionable insights.

## Project Workflow
### 1. Data Creation (SQL Server)

- Designed relational tables: Customers, Accounts, Transactions.

- Inserted 10,000+ synthetic transaction records using recursive CTE.

- Introduced data anomalies:

  -  Mixed date formats (yyyy/MM/dd, dd-MM-yyyy).

  - Inconsistent casing (Credit vs credit, Savings vs savings).

  - Nulls in descriptions, duplicate transaction IDs.

  - Invalid foreign key references (CustomerID=99, AccountID=9999).

  - Outliers in balances & amounts.
 
###  2. Data Cleaning & Transformation

- Removed inconsistencies from date columns.

- Cleaned categorical fields (TransactionType, AccountType, Currency).

- Handled missing values (NULLs in Description).

- Combined data from all three tables with SQL Joins for integrated analysis.

 ### 3. Data Import & Modeling (Power BI)

- Loaded cleaned SQL data into Power BI Desktop.

- Created relationships between Customers, Accounts, and Transactions.

- Built a Measures Table in DAX for KPIs:

  - Total & Average Balance

  - Number of Transactions by Type

  - Transactions by Month

  - Customer Distribution (Gender, Age Group)

  - Inactive Accounts by Month

  - Top 2 Transactions by Name

  - Total Balance by Account Type

### 4. Visualization & Dashboarding

Designed interactive visuals for stakeholders:

- Monthly Transactions Trend

- Customer Segmentation by Age & Gender

- Balance Distribution by Account Type

- Inactive Accounts Analysis

- Top Transactions Ranking

- Tree Map for Customer Distribution

- Published final dashboard to Power BI Service.

 ## Insights

- Identified transaction trends (monthly/weekly).
  <img width="689" height="327" alt="Image" src="https://github.com/user-attachments/assets/36506d52-45d8-4b3f-9a2b-2446167a7179" />

- Segmented customers by age group & gender for targeted offers.

- Tracked inactive accounts over time to improve engagement.

- Detected data quality issues (duplicates, missing values, invalid IDs).

- Measured total balance by account type to understand portfolio health.

## Tools & Technologies

- **SQL Server** → Data creation & preprocessing.

- **Power BI Desktop & Service** → Data modeling, DAX measures, dashboards.

- **DAX** → Custom KPIs & aggregations.

## Conclusion

This project demonstrates how SQL and Power BI can transform messy financial data into clear business insights. From data cleaning and integration to interactive dashboards, the report highlights customer trends, account balances, and transaction patterns to support better decision-making.
