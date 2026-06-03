Task 3: SQL for Data Analysis
📌 Objective

The objective of this task is to use SQL queries to extract meaningful insights from an e-commerce database and perform data analysis using different SQL operations such as filtering, joins, aggregation, subqueries, views, and indexing.

🛠 Tools Used
MySQL / PostgreSQL / SQLite
SQL Editor (MySQL Workbench / pgAdmin / DB Browser for SQLite)
📂 Dataset

Ecommerce_SQL_Database

The dataset contains typical e-commerce fields such as:

Order Date
Category
Region
State
Sales
Profit
Quantity
Customer Name
📌 Tasks Performed
a) Basic SQL Queries

Used fundamental SQL commands:

SELECT
WHERE
ORDER BY
GROUP BY

📌 Example:

SELECT category, SUM(sales) AS total_sales
FROM orders
GROUP BY category
ORDER BY total_sales DESC;
b) Joins (INNER, LEFT, RIGHT)

Combined multiple tables such as Orders, Customers, and Products.

📌 Example:

SELECT o.order_id, c.customer_name, o.sales
FROM orders o
INNER JOIN customers c
ON o.customer_id = c.customer_id;
c) Subqueries

Used nested queries to perform advanced analysis.

📌 Example:

SELECT customer_name, sales
FROM orders
WHERE sales > (SELECT AVG(sales) FROM orders);
d) Aggregate Functions

Used SQL aggregate functions:

SUM()
AVG()
COUNT()
MAX()
MIN()

📌 Example:

SELECT AVG(profit) AS average_profit
FROM orders;
e) Views for Analysis

Created views to simplify repeated analysis queries.

📌 Example:

CREATE VIEW sales_summary AS
SELECT category, SUM(sales) AS total_sales
FROM orders
GROUP BY category;
f) Indexing for Optimization

Improved query performance using indexes.

📌 Example:

CREATE INDEX idx_category
ON orders(category);
📸 Outputs

Screenshots of query results are attached separately in the submission folder.

📊 Key Insights
Identified top-performing product categories
Analyzed regional sales performance
Found high-value customers
Improved query performance using indexing
📁 Deliverables
SQL script file (task3.sql)
Output screenshots
This README file
🚀 Conclusion

This task helped in understanding how SQL can be used for real-world data analysis by combining multiple operations like joins, aggregations, and optimization techniques.