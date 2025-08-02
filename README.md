# Sales Analysis Using SQL

This project analyzes retail sales data using SQL to uncover insights about revenue trends, top customers, product performance, and the impact of discounts and shipping methods.

## Dataset
- Based on the [Superstore Sales Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- Contains order, product, customer, and shipping data

## Objective
To answer key business questions and identify trends using SQL queries:
- Monthly revenue and profit patterns
- Top-performing customers and products
- Regional and category-level sales
- Discount vs. profit relationship
- Shipping mode efficiency

## Tools Used
- SQL (PostgreSQL syntax)
- [Optional] Tableau or Excel for visuals

## Key SQL Concepts
- `GROUP BY`, `JOIN`, `ORDER BY`, `LIMIT`
- Date functions and time series analysis
- Aggregations: `SUM`, `AVG`, `COUNT`
- Window functions (`ROW_NUMBER`)
- CTEs for subqueries

## Files
- `sales_analysis.sql`: All queries used in this project
- `visuals/`: (optional) screenshots of charts or query results

## Example Query
```sql
SELECT DATE_TRUNC('month', order_date) AS month,
       SUM(sales) AS total_revenue
FROM orders
GROUP BY month
ORDER BY month;
