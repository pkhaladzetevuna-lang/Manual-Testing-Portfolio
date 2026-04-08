# 🗄️ SQL Queries for QA Testing Portfolio

This document showcases my proficiency in SQL for database testing. It covers data verification, complex joins, and backend validation scenarios.

---

## 🛠 Database Operations Overview
* **DQL (Data Query Language):** SELECT, FROM, WHERE, JOIN
* **DML (Data Manipulation Language):** INSERT, UPDATE, DELETE
* **Aggregations:** COUNT, SUM, AVG, GROUP BY, HAVING
* **Sorting:** ORDER BY (ASC/DESC)

---

## 📝 Practice Scenarios & Queries

### 1. Simple Data Verification
**Scenario:** Check if a user exists and is active.
```sql
SELECT id, email, first_name, status 
FROM users 
WHERE email = 'teona.p@example.com' 
AND status = 'active';
2. Pattern Matching (Search Validation)
Scenario: Find all users whose email ends with '@gmail.com'.

SQL
SELECT * FROM users 
WHERE email LIKE '%@gmail.com';
3. Joining Tables (The most important QA skill)
Scenario: Retrieve order details along with the user's name and product name.

SQL
SELECT 
    u.first_name, 
    u.last_name, 
    o.order_id, 
    p.product_name, 
    o.order_date
FROM users u
INNER JOIN orders o ON u.id = o.user_id
INNER JOIN products p ON o.product_id = p.id
WHERE u.id = 505
ORDER BY o.order_date DESC;
4. Aggregation & Grouping
Scenario: Count how many orders were made in each status (e.g., Pending, Shipped, Delivered).

SQL
SELECT status, COUNT(order_id) AS total_orders
FROM orders
GROUP BY status
HAVING COUNT(order_id) > 0;
5. Boundary Value Testing (Dates)
Scenario: Find all transactions made between two specific dates.

SQL
SELECT transaction_id, amount, created_at
FROM payments
WHERE created_at BETWEEN '2026-01-01' AND '2026-03-31'
ORDER BY created_at ASC;
6. Data Integrity Check (Subqueries)
Scenario: Find users who have never placed an order.

SQL
SELECT email FROM users
WHERE id NOT IN (SELECT DISTINCT user_id FROM orders);
7. Backend Validation (Update/Delete)
Scenario: Verify if a user's role was updated to 'Admin'.

SQL
-- Step 1: Update role
UPDATE users SET role = 'admin' WHERE id = 77;

-- Step 2: Verify update
SELECT id, email, role FROM users WHERE id = 77;
