Sure 👍
Below is a clean, correct EMPLOYEE table creation + sample data, exactly matching what Experiment 5 needs.

You can run this once, then all Experiment-5 queries will work perfectly.


---

## EMPLOYEE TABLE CREATION (For Experiment 5)

### Create EMPLOYEE Table
```sql
CREATE TABLE Employee (
  Emp_No INT PRIMARY KEY,
  Emp_Name VARCHAR(20),
  Address VARCHAR(20),
  Sex CHAR(1),
  Dept VARCHAR(20),
  Salary INT,
  DOJ DATE,
  Branch VARCHAR(20)
);


---

Insert Sample Records into EMPLOYEE

INSERT INTO Employee VALUES
(1001, 'Aysha', 'Pal', 'F', 'HR', 34000, '2017-12-02', 'Finance'),
(1002, 'Arjun', 'Ern', 'M', 'Coding', 40000, '2019-10-12', 'IT'),
(1003, 'Teena', 'Knr', 'F', 'Sales', 30000, '2016-12-22', 'Marketing'),
(1004, 'Rahul', 'Koz', 'M', 'Clerk', 25000, '2019-05-15', 'Finance'),
(1005, 'Anu', 'Pal', 'F', 'Design', 15000, '2022-11-25', 'IT');


---

View EMPLOYEE Table Structure

DESC Employee;


---

EMPLOYEE Table After Insertion

SELECT * FROM Employee;

Emp_No	Emp_Name	Address	Sex	Dept	Salary	DOJ	Branch

1001	Aysha	Pal	F	HR	34000	2017-12-02	Finance
1002	Arjun	Ern	M	Coding	40000	2019-10-12	IT
1003	Teena	Knr	F	Sales	30000	2016-12-22	Marketing
1004	Rahul	Koz	M	Clerk	25000	2019-05-15	Finance
1005	Anu	Pal	F	Design	15000	2022-11-25	IT


---

This table **fully supports all queries in Experiment 5**  
(`DISTINCT`, `IN`, `NOT IN`, `BETWEEN`, `ORDER BY`, etc.).

If you want, I can:
- 🔹 Adjust data to **match exactly your college record**
- 🔹 Add **constraints (NOT NULL, CHECK)**
- 🔹 Prepare **Experiment 6** next in same Markdown style

Just say 👍
