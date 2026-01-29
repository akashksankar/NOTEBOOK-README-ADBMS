

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

```


