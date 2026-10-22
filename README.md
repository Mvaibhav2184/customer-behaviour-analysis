# E-Commerce Customer Behaviour Analysis

## About the Project

This project focuses on analysing e-commerce transaction data using SQL Server and Python. The goal is to clean and prepare transaction data, understand customer purchasing behaviour, and group customers based on their buying patterns using RFM analysis.

**Project status:** Work in Progress

## Tools Used

- Microsoft SQL Server
- SQL
- Python
- Pandas
- Jupyter Notebook
- Microsoft Excel

## What I Did

### 1. Data Cleaning Using SQL

- Combined transaction data from 2009–2010 and 2010–2011 into a single table.
- Converted date and price columns into appropriate data types using `TRY_CONVERT()` and `COALESCE()`.
- Checked row counts, invalid dates, invalid prices and duplicate records.
- Used `GROUP BY`, `HAVING` and `ROW_NUMBER()` to identify and remove exact duplicate records.
- Created a cleaned table named `RetailCleaned`.

### 2. Customer Analysis Using Python

- Loaded and inspected the transaction data using Pandas.
- Filtered records with missing customer IDs and non-positive quantities.
- Calculated RFM metrics for each customer:
  - **Recency:** How recently a customer purchased.
  - **Frequency:** How many distinct invoices a customer had.
  - **Monetary:** Total transaction value.
- Assigned scores from 1 to 5 for each RFM metric.
- Grouped customers into six segments: Champions, Loyal, At Risk, New, Needs Attention and Lost.
- Created a churn flag for customers whose last purchase was more than 90 days before the snapshot date.


## Project Files

- `RFM segmentation.py` – Python code for RFM analysis and customer segmentation.
- `customer_analysis.ipynb` – Jupyter Notebook, if included.
- `ecommerce_dashboard_data.xlsx` – Processed analytical output.
- `README.md` – Project documentation.
- 
## Key Learning

Through this project, I practised SQL data cleaning, type conversion, duplicate detection,  data aggregation using Pandas, quantile-based scoring and rule-based customer segmentation.

## Future Improvements

- Analyse customer segment distribution and revenue contribution.
- Add visualisations and business insights.
- Build a Power BI dashboard.
- Validate the segmentation rules and explore predictive churn analysis.

