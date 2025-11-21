##Task 6 – Sales Trend Analysis

Objective
Analyze monthly revenue and monthly order volume using SQL.

Main SQL Query
SELECT
    EXTRACT(YEAR FROM order_date) AS year,
    EXTRACT(MONTH FROM order_date) AS month,
    SUM(amount) AS total_revenue,
    COUNT(DISTINCT order_id) AS order_volume
FROM 
    online_sales
GROUP BY 
    EXTRACT(YEAR FROM order_date), EXTRACT(MONTH FROM order_date)
ORDER BY 
    year, month;

Files Included
  1)monthly_summary.csv
  2)monthly_summary.sql
  3)screenshots
