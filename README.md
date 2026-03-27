# SQL-QUERIES-
✅ Queries 
✅ Output tables (after each query) 
✅ Simple explanations 
✅ Clause definitions

# 📘 SQL Learning Notes (CRUD + Clauses + Practice)

A beginner-friendly guide covering SQL basics with examples, outputs, and explanations.

---

##  1. Create Database & Table

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
