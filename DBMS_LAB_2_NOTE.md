

---

````md
# MCA DBMS Notes – MySQL (DDL & DML Commands)

## 1. Database Management (DDL – Database Level)

### List All Databases
```sql
SHOW DATABASES;
````

### Select a Database

```sql
USE COMPANY3;
```

---

## 2. Table Definition (DDL – Data Definition Language)

### Create Table

```sql
CREATE TABLE DEPARTMENT (
    Dept_No INT PRIMARY KEY,
    Dname VARCHAR(20),
    Mgr_id INT,
    mgr_strtdate DATE
);
```

**Concepts Used:**

* `INT`, `VARCHAR`, `DATE` data types
* `PRIMARY KEY` constraint

---

## 3. Data Insertion (DML – Data Manipulation Language)

### Insert Multiple Records

```sql
INSERT INTO DEPARTMENT VALUES
(101, 'HR', 20063, '2016-12-11'),
(102, 'IT', 34063, '2020-11-21'),
(103, 'finance', 52101, '2009-01-13'),
(104, 'sales', 15201, '2022-07-10'),
(105, 'finance', 56564, '2022-10-11');
```

---

## 4. Data Retrieval (DQL – Data Query Language)

### Display All Records

```sql
SELECT * FROM DEPARTMENT;
```

---

## 5. Data Modification (DML)

### Update Table Data

```sql
UPDATE DEPARTMENT
SET Mgr_id = 45621
WHERE Dept_No = 104;
```

### Update Specific Attribute Values

```sql
UPDATE Dept
SET Dname = 'Human Resource'
WHERE Dname = 'HR';
```

---

## 6. Table Alteration (DDL)

### Rename Table

```sql
ALTER TABLE DEPARTMENT RENAME TO Dept;
```

---

## 7. Data Deletion (DML)

### Delete a Record

```sql
DELETE FROM Dept
WHERE Dept_No = 104;
```

---

## 8. Final Data View

### Display Updated Table

```sql
SELECT * FROM Dept;
```

---

## 9. MCA DBMS Syllabus Mapping

### DDL Commands

* `CREATE TABLE`
* `ALTER TABLE`
* `RENAME TABLE`

### DML Commands

* `INSERT`
* `UPDATE`
* `DELETE`

### DQL Commands

* `SELECT`

### Database Commands

* `SHOW DATABASES`
* `USE database_name`

---

## 10. Key Learning Outcomes (Exam Ready)

* Creation and management of relational tables
* Use of primary key constraints
* Performing insert, update, and delete operations
* Understanding table modification using `ALTER`
* Applying SQL commands in a real DBMS environment

---


````md
# MCA DBMS Notes – Course & Student Marks (MySQL)

## 1. Course Table (DDL)

### Create `Course` Table
```sql
CREATE TABLE Course (
    Course_ID INT PRIMARY KEY,
    Course_Name VARCHAR(50),
    Program_ID INT,
    Credit INT,
    Semester INT,
    Internal_Mark INT,
    External_Mark INT,
    Course_Type VARCHAR(20)
);
````

### View Table Structure

```sql
DESC Course;
```

---

## 2. Student_Mark Table (DDL with Foreign Key)

### Create `Student_Mark` Table

```sql
CREATE TABLE Student_Mark (
    Reg_No INT PRIMARY KEY,
    Course_ID INT,
    Program_ID INT,
    Student_Internal INT,
    Student_External INT,
    FOREIGN KEY (Course_ID) REFERENCES Course(Course_ID)
);
```

### View Table Structure

```sql
DESC Student_Mark;
```

---

## 3. Data Insertion (DML)

### Insert Records into `Course`

```sql
INSERT INTO Course VALUES
(501, 'DBMS', 10, 4, 3, 30, 70, 'core'),
(502, 'Network', 10, 4, 3, 30, 70, 'elective'),
(503, 'web', 11, 3, 5, 35, 72, 'core');
```

### Insert Records into `Student_Mark`

```sql
INSERT INTO Student_Mark VALUES
(202401, 501, 10, 25, 65),
(202402, 501, 10, 28, 60),
(202403, 501, 10, 27, 61);
```

---

## 4. Data Retrieval (DQL)

### Display Course Table

```sql
SELECT * FROM Course;
```

### Display Student Marks

```sql
SELECT * FROM Student_Mark;
```

---

## 5. MCA DBMS Syllabus Mapping

### DDL Commands

* `CREATE TABLE`
* `PRIMARY KEY`
* `FOREIGN KEY`
* `DESC`

### DML Commands

* `INSERT INTO`

### DQL Commands

* `SELECT`

---

## 6. Key Concepts Covered (Exam Oriented)

* Entity creation using `CREATE TABLE`
* Primary Key constraint
* Foreign Key constraint (Referential Integrity)
* One-to-Many relationship (Course → Student_Mark)
* Insertion and retrieval of relational data

---

```




