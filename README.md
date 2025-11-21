

## 📊 Task 6 – Sales Trend Analysis (MySQL)
📌 Objective
Analyze monthly revenue and monthly order volume using SQL using the online_sales dataset.

## Dataset
Table: online_sales
Columns:
order_id
order_date
amount
product_id

## Steps Performed
Created the online_sales table
Inserted sample sales data (20 records)
Displayed full dataset
Calculated total monthly revenue using SUM(amount)
Calculated monthly order volume using COUNT(DISTINCT order_id)
Grouped results by year and month
Sorted results in ascending order
Identified top 3 months based on revenue
Exported monthly summary as CSV
Added SQL, CSV, and screenshots to GitHub


## Main SQL Query (Monthly Revenue & Volume)
SELECT
EXTRACT(YEAR FROM order_date) AS year,
EXTRACT(MONTH FROM order_date) AS month,
SUM(amount) AS total_revenue,
COUNT(DISTINCT order_id) AS order_volume
FROM online_sales
GROUP BY EXTRACT(YEAR FROM order_date), EXTRACT(MONTH FROM order_date)
ORDER BY year, month;


## Top 3 Revenue Months Query
SELECT
EXTRACT(YEAR FROM order_date) AS year,
EXTRACT(MONTH FROM order_date) AS month,
SUM(amount) AS revenue
FROM online_sales
GROUP BY EXTRACT(YEAR FROM order_date), EXTRACT(MONTH FROM order_date)
ORDER BY revenue DESC
LIMIT 3;


## Files Included in Repository
monthly_summary.csv
monthly_summary.sql
screenshot_full_table.png
screenshot_monthly_summary.png
screenshot_top3.png
README.md


## Output Summary
Analysis performed using MySQL
Revenue and order volume calculated correctly
Top 3 months identified
CSV file generated
Repository files organized correctly

 ## AUTHOR
 Bingi Manoj



