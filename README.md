# Sql-5th-task


## 📄 README: SQL Joins with Related Tables


### ✅ 1. Creating Related Tables

Two tables were created:

* **Customers** – stores customer details with a primary key `customer_id`.
* **Orders** – stores product orders with a foreign key `customer_id` referencing the Customers table.

This setup creates a **one-to-many relationship** where one customer can have multiple orders.



# 2. SQL JOIN Types

Joins are used to combine data from related tables based on a common key.

# INNER JOIN

Retrieves only the records where there is a match in both tables.
Example: Customers who have placed at least one order.

# LEFT JOIN

Retrieves **all records from the left table** (Customers) and matched records from the right table (Orders).
Unmatched right-side values will be shown as NULL.
Example: Lists all customers, including those who haven’t placed an order.

# RIGHT JOIN

Retrieves **all records from the right table** (Orders) and matched records from the left table (Customers).
Unmatched left-side values will be shown as NULL.
Example: Useful if some orders might not have valid customer entries.

# FULL JOIN

Returns **all records from both tables**, matched where possible, and fills with NULL where no match exists.
Not directly supported in MySQL, but can be simulated using `UNION` of `LEFT JOIN` and `RIGHT JOIN`.

