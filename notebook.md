# MySQL Terminal Session Summary

## 1. MySQL Login
- Attempted to log in as normal user:
  - ❌ Access denied for user `student` (no password provided)
- Successfully logged in using superuser privileges:
  - ✅ `sudo mysql`
  - MySQL Server Version: **8.0.42 (Ubuntu 20.04)**

---

## 2. Database Selection
- Initial attempt to create a table failed:
  - ❌ Error: **No database selected**
- Database selected successfully:
  - ✅ `USE COMPANY3;`

---

## 3. Table: `employees1`
### Creation
- Created table `employees1` with the following fields:
  - `id` (INT, Primary Key, Auto Increment)
  - `name` (VARCHAR(100), NOT NULL)
  - `salary` (DECIMAL(10,2))
  - `department` (VARCHAR(50))
  - `phone_number` (VARCHAR(20))

### Description
- Table structure verified using `DESC employees1;`
- Table contains **5 columns** and was created successfully

---

## 4. Syntax Error Encountered
- Incorrect table creation syntax for `DEPARTMENT` table:
  - ❌ SQL syntax error due to missing data types

---

## 5. Table: `college_departments`
### Creation
- Created table `college_departments` with fields:
  - `dept_no` (INT, Primary Key)
  - `dept_name` (VARCHAR(100), NOT NULL)
  - `hod_name` (VARCHAR(100))
  - `teacher_name` (VARCHAR(100))

### Data Insertion
- Inserted **5 records** representing different college departments

### Data Retrieval
- `SELECT * FROM college_departments;` displayed:
  - Computer Science
  - Mathematics
  - Physics
  - Mechanical Engineering
  - Civil Engineering

---

## ✅ Final Outcome
- Successfully connected to MySQL using sudo
- Created and verified two tables
- Inserted and retrieved data correctly
- Identified and corrected SQL syntax errors

