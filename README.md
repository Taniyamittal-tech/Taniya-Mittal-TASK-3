# Taniya-Mittal-TASK-3
<br>
1. Select Data from a Table
<br>
<br>
SELECT * FROM sales;
<br>
<br>
This retrieves all columns from the sales table.
<br>
<br>
2. Filter Data Using WHERE
<br>
<br>
SELECT * FROM sales
<br>
WHERE sale_date >= '2024-01-01' AND
<br>
sale_date <= '2024-12-31';
  <br>
  <br>
Filters records for the year 2024.
<br>
<br>
3. Aggregate Data (SUM, AVG, COUNT, etc.)
<br>
  <br>
SELECT 
  <br>
    product_id,
  <br>
    SUM(sale_amount) AS total_sales,
  <br>
    COUNT(*) AS total_transactions
  <br>
FROM sales
  <br>
GROUP BY product_id;
  <br>
<br>
Gives total sales and transaction count per product.
<br>
<br>
4. Order Results
<br>
  <br>
SELECT product_id, SUM(sale_amount)
  <br>
  AS total_sales
  <br>
FROM sales
  <br>
GROUP BY product_id
  <br>
ORDER BY total_sales DESC;
<br>
  <br>
Sorts products by total sales in descending order.
<br>
<br>
5. Join Tables
<br>
  <br>
Assume we have a products table and sales table.
<br>
  <br>
SELECT 
  <br>
    p.product_name,
  <br>
    s.sale_amount,
  <br>
    s.sale_date
  <br>
FROM sales s
  <br>
JOIN products p ON s.product_id =
  <br>
  p.product_id;
  <br>
<br>
Combines data from sales and products to include product names.
<br>
<br>
6. Use Subqueries
<br>
  <br>
SELECT product_id, sale_amount
  <br>
FROM sales
  <br>
WHERE sale_amount > (
  <br>
    SELECT AVG(sale_amount) FROM
  <br>
  sales
  <br>
);
<br>
  <br>
Find sales with above- average amounts.
<br>
<br>
7. Date Functions
<br>
  <br>
SELECT 
  <br>
    MONTH(sale_date) AS month,
  <br>
    SUM(sale_amount) AS 
  <br>
  monthly_sales
  <br>
FROM sales
  <br>
GROUP BY MONTH(sale_date);
<br>
  <br>
Summarizes monthly sales totals.

