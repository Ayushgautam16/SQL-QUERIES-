# SQL-QUERIES-
✅ Queries 
✅ Output tables (after each query) 
✅ Simple explanations 
✅ Clause definitions

# 📘 SQL Learning Notes (CRUD + Clauses + Practice)

A beginner-friendly guide covering SQL basics with examples, outputs, and explanations.

---

## 1. Create Database & Table
```sql
CREATE DATABASE students;

CREATE TABLE students (
  name CHAR(30),
  age INT,
  grade CHAR(1),
  student_id INT
);


 2. Insert Data
INSERT INTO students(student_id, name, age, grade)
VALUES 
(11, 'ayush', 23, 'A'),
(12, 'akash', 22, 'B'),
(13, 'anjali', 24, 'C');

Output-

| student_id | name   | age | grade |
| ---------- | ------ | --- | ----- |
| 11         | ayush  | 23  | A     |
| 12         | akash  | 22  | B     |
| 13         | anjali | 24  | C     |

3. Update Query

UPDATE students
SET name = 'Anmol'
WHERE age = 24;

Output

| student_id | name  | age | grade |
| ---------- | ----- | --- | ----- |
| 11         | ayush | 23  | A     |
| 12         | akash | 22  | B     |
| 13         | Anmol | 24  | C     |

4. Select Query
SELECT * FROM students;

Output

| student_id | name  | age | grade |
| ---------- | ----- | --- | ----- |
| 11         | ayush | 23  | A     |
| 12         | akash | 22  | B     |
| 13         | Anmol | 24  | C     |

5. Update Multiple Rows

UPDATE students
SET student_id = 2
WHERE age = 23;

Output

| student_id | name  | age | grade |
| ---------- | ----- | --- | ----- |
| 2          | ayush | 23  | A     |
| 12         | akash | 22  | B     |
| 13         | Anmol | 24  | C     |

6. Delete Query

DELETE FROM students
WHERE name = 'ayush';

Output

| student_id | name  | age | grade |
| ---------- | ----- | --- | ----- |
| 12         | akash | 22  | B     |
| 13         | Anmol | 24  | C     |

CRUD Operations
Create → INSERT
Read → SELECT
Update → UPDATE
Delete → DELETE

7. Data Types

Numeric Types-

SMALLINT
INT
BIGINT
DECIMAL(p,s)
NUMERIC(p,s)
REAL
DOUBLE PRECISION
SERIAL


String Types

CREATE TABLE strings (
  code CHAR(5),
  email VARCHAR(100),
  bio TEXT
);

8. Constraints Example

CREATE TABLE random(
  id INT PRIMARY KEY,
  name VARCHAR(199) NOT NULL,
  email TEXT UNIQUE,
  created_at DATE DEFAULT NOW(),
  age INT CHECK(age >= 18)
);

9. Products Table-

CREATE TABLE products(
  product_id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  sku_code CHAR(8) UNIQUE NOT NULL,
  price NUMERIC(10,2) CHECK (price > 0),
  stock_quantity INT DEFAULT 0 CHECK (stock_quantity >= 0),
  is_available BOOLEAN DEFAULT TRUE,
  category TEXT NOT NULL,
  added_on DATE DEFAULT CURRENT_DATE,
  last_update TIMESTAMP DEFAULT NOW()
);

Insert Data-

INSERT INTO products (name, sku_code, price, stock_quantity, is_available, category)
VALUES

('Wireless Mouse', 'WM123456', 699.99, 50, TRUE, 'Electronics'),
('Bluetooth Speaker', 'BS234567', 1499.00, 30, TRUE, 'Electronics'),
('Laptop Stand', 'LS345678', 799.50, 20, TRUE, 'Accessories'),
('USB-C Hub', 'UC456789', 1299.99, 15, TRUE, 'Accessories'),
('Notebook', 'NB567890', 99.99, 100, TRUE, 'Stationery'),
('Pen Set', 'PS678901', 199.00, 200, TRUE, 'Stationery'),
('Coffee Mug', 'CM789012', 299.00, 75, TRUE, 'Home & Kitchen'),
('LED Desk Lamp', 'DL890123', 899.00, 40, TRUE, 'Home & Kitchen'),
('Yoga Mat', 'YM901234', 499.00, 25, TRUE, 'Fitness'),
('Water Bottle', 'WB012345', 349.00, 60, TRUE, 'Fitness');

10. GROUP BY + HAVING

SELECT category, COUNT(*) 
FROM products
GROUP BY category
HAVING COUNT(*) > 1;


Output-

| category       | count |
| -------------- | ----- |
| Electronics    | 2     |
| Accessories    | 2     |
| Stationery     | 2     |
| Home & Kitchen | 2     |
| Fitness        | 2     |


11. ORDER BY

SELECT * FROM products ORDER BY price DESC;


12. LIMIT

SELECT * FROM products LIMIT 3;


Output-

| name              | price   |
| ----------------- | ------- |
| Wireless Mouse    | 699.99  |
| Bluetooth Speaker | 1499.00 |
| Laptop Stand      | 799.50  |


13. ALIAS (AS)

SELECT name AS item_name, price AS item_price FROM products;


14. DISTINCT
SELECT DISTINCT category FROM products;


Output-

| category       |
| -------------- |
| Electronics    |
| Accessories    |
| Stationery     |
| Home & Kitchen |
| Fitness        |


15. SQL Clauses (Simple Definitions)

HAVING - Filters grouped data (used with GROUP BY)

HAVING COUNT(*) > 1;

16. ORDER BY - Sorts data (ASC / DESC)

ORDER BY price DESC;

17. LIMIT - Limits number of rows
LIMIT 3;

18. AS (Alias) Renames columns temporarily

name AS item_name;

19. DISTINCT Removes duplicate values

SELECT DISTINCT category;

20. Final Note This guide covers:

CRUD operations
Data types
Constraints
SQL clauses
Real-world examples





