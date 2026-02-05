Perfect 👍
Below is a fully simplified, clean, exam-ready Experiment 3, written entirely in Markdown, exactly in DBMS lab record style.

You can copy–paste this directly into your record / Markdown file.


---

# EXPERIMENT NO: 3

## AIM
To create schemas **COURSE** and **STUDENT_MARK**, associate them using a **foreign key**, and perform **insertion, updation, deletion, and alteration** operations.

---

## DATABASE USED
```sql
USE company;


---

TABLE CREATION

1. Create COURSE Table

CREATE TABLE course (
  Course_ID VARCHAR(15) PRIMARY KEY,
  Course_Name VARCHAR(20) NOT NULL,
  Program_ID SMALLINT,
  Credit SMALLINT,
  Semester VARCHAR(10),
  Internal_mark INT,
  External_mark INT,
  Course_Type VARCHAR(10)
);

Structure of COURSE Table

DESC course;

Field	Type

Course_ID	varchar(15)
Course_Name	varchar(20)
Program_ID	smallint
Credit	smallint
Semester	varchar(10)
Internal_mark	int
External_mark	int
Course_Type	varchar(10)



---

2. Create STUDENT_MARK Table

CREATE TABLE Student_Mark (
  Reg_No VARCHAR(10) PRIMARY KEY,
  Course_ID VARCHAR(15),
  Student_Internal INT NOT NULL,
  Student_External INT NOT NULL,
  FOREIGN KEY (Course_ID) REFERENCES course(Course_ID)
);

Structure of STUDENT_MARK Table

DESC Student_Mark;

Field	Type

Reg_No	varchar(10)
Course_ID	varchar(15)
Student_Internal	int
Student_External	int



---

DATA INSERTION

Insert Records into COURSE

INSERT INTO course VALUES
('mca1', 'MCA', 200, 4, 's2', 45, 55, 'Integrate'),
('mca2', 'MCA', 201, 6, 's4', 40, 60, 'Regular'),
('bca3', 'BCA', 202, 8, 's3', 60, 40, 'Regular'),
('btech4', 'Btech', 203, 6, 's4', 50, 50, 'Lateral');

COURSE Table After Insertion

SELECT * FROM course;

Course_ID	Course_Name	Program_ID	Credit	Semester	Internal	External	Type

mca1	MCA	200	4	s2	45	55	Integrate
mca2	MCA	201	6	s4	40	60	Regular
bca3	BCA	202	8	s3	60	40	Regular
btech4	Btech	203	6	s4	50	50	Lateral



---

Insert Records into STUDENT_MARK

INSERT INTO Student_Mark VALUES
('b123', 'mca1', 35, 40),
('m141', 'mca2', 28, 42),
('mi768', 'bca3', 34, 52),
('mt836', 'btech4', 55, 48);

STUDENT_MARK Table After Insertion

SELECT * FROM Student_Mark;

Reg_No	Course_ID	Internal	External

b123	mca1	35	40
m141	mca2	28	42
mi768	bca3	34	52
mt836	btech4	55	48



---

UPDATE OPERATIONS

Update Semester in COURSE

UPDATE course
SET Semester = 's4'
WHERE Course_ID = 'bca3';

Update Internal Mark in STUDENT_MARK

UPDATE Student_Mark
SET Student_Internal = 28
WHERE Reg_No = 'mt836';


---

ALTER OPERATIONS

Rename Column in COURSE

ALTER TABLE course
CHANGE Course_Name Course_Name VARCHAR(20);

Add New Column in STUDENT_MARK

ALTER TABLE Student_Mark
ADD Result VARCHAR(10);

Drop Column from STUDENT_MARK

ALTER TABLE Student_Mark
DROP Result;


---

RENAME TABLE

RENAME TABLE Student_Mark TO std_mark;


---

DELETE OPERATIONS

Delete All Records

TRUNCATE TABLE std_mark;

Drop Table

DROP TABLE course;


---

RESULT

The schemas COURSE and STUDENT_MARK were created successfully, associated using foreign key constraints, and all required DDL and DML operations were performed successfully.

---

If you want next:
- ✅ **Even shorter version (2–3 pages max)**
- ✅ **KTU-style handwritten format**
- ✅ **Screenshots command order**
- ✅ **Viva questions for Experiment 3**

Just say the word 👌
