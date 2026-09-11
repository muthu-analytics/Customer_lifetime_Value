# 💎 Customer Lifetime Value (CLV) Dashboard — Power BI

An interactive Power BI dashboard that helps understand **customer value, buying behavior, and retention** in an online retail business. It uses Customer Lifetime Value (CLV) and RFM analysis to identify different customer groups and understand their contribution to the business.

## 📌 Business Problem

Online retail reports often focus on sales and transactions. But sales numbers alone do not show the complete customer picture.

The business needs to understand:

* Which customers are more valuable to the business?
* How often do customers make purchases?
* Which customers are active or inactive?
* How many customers make repeat purchases?
* Which customer segments contribute the most revenue?
* How does customer value change over time?
* Which customers may need more attention for retention?

Without this information, it can be difficult to plan effective customer retention and marketing strategies.

## 🎯 Objective

The main objective of this project is to build an interactive Power BI dashboard that helps the business:

* Calculate Customer Lifetime Value (CLV) at the customer level
* Understand customer purchasing behavior
* Identify High, Medium, and Low-value customers
* Compare customer segments and their revenue contribution
* Analyze repeat, one-time, active, and inactive customers
* Understand customer retention patterns
* Analyze customer value over time
* Explore individual customers using drill-through analysis

## 📊 Dataset

**Source:** [Online Retail II](https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset) — CRM Analytics (CLTV), via Kaggle (author: Halime Dogan)

The dataset contains online retail transaction data with the following fields:

| Column      | Description                                                        |
| ----------- | ------------------------------------------------------------------ |
| Invoice     | Invoice number. Invoices starting with "C" represent cancellations |
| StockCode   | Product code                                                       |
| Description | Product name                                                       |
| Quantity    | Number of units purchased                                          |
| InvoiceDate | Date and time of the transaction                                   |
| UnitPrice   | Product price in GBP                                               |
| CustomerID  | Unique customer ID                                                 |
| Country     | Customer's country                                                 |

The two yearly datasets were combined into one table for analysis.

## 🧼 Data Cleaning

Data cleaning was performed using **Power Query in Power BI**.

Main cleaning steps:

1. Loaded both yearly sheets and combined them into one table
2. Standardized column names
3. Removed records with missing Customer IDs
4. Changed columns to the correct data types
5. Created an `Is_Cancelled` column to identify cancelled orders
6. Removed records with zero or negative prices
7. Removed duplicate rows
8. Created a `Total_Amount` column using `Quantity × Price`
9. Removed extra spaces from text columns
10. Removed rows with blank product descriptions
11. Loaded the cleaned data into the Power BI data model

Detailed cleaning steps are available in `Cleaning_steps_in_power_query.txt`.

## 📈 Dashboard

The dashboard contains **two interactive pages**.

### Page 1 — Customer Lifetime Value Overview

This page provides an overall view of customer value and business performance.

**Key visuals:**

* Total Customers — 6K
* Revenue — 17.37M
* Total Orders — 37K
* Average Order Value — 469.98
* Repeat Rate — 72.39%
* Top 10 Customers by Lifetime Value
* Revenue Growth Trend
* Revenue by Country
* Revenue by Customer Segment
* Customer Segment Distribution
* Year, Month, and Country slicers

### Page 2 — Customer Behavior & Retention

This page focuses on customer activity, purchasing behavior, and retention.

**Key visuals:**

* Repeat Rate
* Active Customers — 3K
* Inactive Customers — 3K
* Active Rate — 49.15%
* Average Purchase Frequency — 1.14
* Average Recency — 200.87 days
* Customer Value Distribution
* Active Customers Over Time
* Loyalty Patterns by Value Segment
* Purchase Frequency vs. Customer Value
* Active vs. Inactive Customers
* CLV vs. RFM Segment Comparison
* Country, Month, and Year slicers

## 🎯 RFM Segmentation

The dashboard also uses **RFM analysis** to understand customer behavior.

RFM stands for:

* **Recency** — How recently a customer purchased
* **Frequency** — How often a customer purchased
* **Monetary** — How much value the customer generated

Each customer receives an RFM score, which is then used to group customers into segments such as:

* **Champions**
* **Loyal / Steady**
* **At Risk / Low Engagement**

Customers are also grouped into **High, Medium, and Low CLV segments** to understand differences in customer value.

## 🗂️ Repository Structure

```text
├── customer_lifetime_value.pbix
├── Cleaning_steps_in_power_query.txt
├── Final_Problem_statement.docx
├── Customer_Lifetime_Value_Dashboard.pptx
└── README.md
```

## 🛠️ Tools Used

* Power BI
* Power Query
* DAX
* Data Modeling
* Dashboard Design

## 💡 Key Business Insights

The analysis helps identify:

* High-value customers who contribute more to revenue
* Differences in revenue contribution across customer segments
* Repeat and one-time customer behavior
* Active and inactive customers
* Changes in revenue over time
* Customers with different purchasing frequencies
* Customer groups that may need more attention for retention

## 🚀 Business Value

This dashboard changes the focus from **individual transactions to customer-level analysis**.

It helps the business understand **who the valuable customers are, how they behave, and which customer groups may need more attention**. These insights can support more targeted customer retention, marketing, and resource-planning decisions.

## 📌 Project Outcome

This project helped me practice:

* Customer Lifetime Value analysis
* RFM analysis
* Customer segmentation
* Retention analysis
* DAX calculations
* Power Query data cleaning
* Data modeling
* Interactive dashboard development
* Business insight generation

---

*Thank you for exploring this project. Feedback and suggestions are always welcome!*
