# 🗄️ SQL Queries for QA Testing Portfolio

This document showcases my proficiency in SQL for database testing. It covers data verification, complex joins, and backend validation scenarios.

---

### 1. Simple Data Verification
**Scenario:** Check if a user exists and is active in the system.
```sql
SELECT id, email, first_name, status 
FROM users 
WHERE email = 'teona.p@example.com' 
AND status = 'active';
2. Pattern Matching (Search Validation)
Scenario: Find all users whose email ends with '@gmail.com' to verify search/filter logic.

SQL
SELECT * FROM users 
WHERE email LIKE '%@gmail.com';
3. Joining Tables (Relational Data Testing)
Scenario: Retrieve order details along with the user's name and product name to verify database relationships.

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
Scenario: Count how many orders were made in each status (Pending, Shipped, Delivered) for reporting accuracy.

SQL
SELECT status, COUNT(order_id) AS total_orders
FROM orders
GROUP BY status
HAVING COUNT(order_id) > 0;
5. Boundary Value Testing (Dates)
Scenario: Find all transactions made between specific dates to verify period-based filters.

SQL
SELECT transaction_id, amount, created_at
FROM payments
WHERE created_at BETWEEN '2026-01-01' AND '2026-03-31'
ORDER BY created_at ASC;
6. Data Integrity Check (Subqueries)
Scenario: Identify users who have never placed an order (checking for orphaned or inactive accounts).

SQL
SELECT email FROM users
WHERE id NOT IN (SELECT DISTINCT user_id FROM orders);
7. Backend Validation (Update/Delete)
Scenario: Verify if a user's role was successfully updated in the database.

SQL
-- Step 1: Update role to Admin
UPDATE users SET role = 'admin' WHERE id = 77;

-- Step 2: Verify the change immediately
SELECT id, email, role FROM users WHERE id = 77;
