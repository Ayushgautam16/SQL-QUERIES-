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






