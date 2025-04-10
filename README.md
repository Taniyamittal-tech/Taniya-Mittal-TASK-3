# Taniya-Mittal-TASK-3
<br>
1. Select Data from a Table
<br>
SELECT * FROM sales;
<br>
This retrieves all columns from the sales table.
<br>
<br>
2. Filter Data Using WHERE
<br>
SELECT * FROM sales
<br>
WHERE sale_date >= '2024-01-01' AND sale_date <= '2024-12-31';
  <br>
Filters records for the year 2024.
<br>
<br>
3. Aggregate Data (SUM, AVG, COUNT, etc.)
<br>
SELECT 
    product_id,
    SUM(sale_amount) AS total_sales,
    COUNT(*) AS total_transactions
FROM sales
GROUP BY product_id;
<br>
Gives total sales and transaction count per product.
<br>
<br>
4. Order Results
<br>
SELECT product_id, SUM(sale_amount) AS total_sales
FROM sales
GROUP BY product_id
ORDER BY total_sales DESC;
<br>
Sorts products by total sales in descending order.
<br>
<br>
5. Join Tables
<br>
Assume we have a products table and sales table.
<br>
SELECT 
    p.product_name,
    s.sale_amount,
    s.sale_date
FROM sales s
JOIN products p ON s.product_id = p.product_id;
<br>
Combines data from sales and products to include product names.
<br>
<br>
6. Use Subqueries
<br>
SELECT product_id, sale_amount
FROM sales
WHERE sale_amount > (
    SELECT AVG(sale_amount) FROM sales
);
<br>
Find sales with above- average amounts.
<br>
<br>
7. Date Functions
<br>
SELECT 
    MONTH(sale_date) AS month,
    SUM(sale_amount) AS monthly_sales
FROM sales
GROUP BY MONTH(sale_date);
<br>
Summarizes monthly sales totals.

