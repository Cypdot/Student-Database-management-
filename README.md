# LITA_CLASS_Document

### Project Title: Student Database Management
---

### Project Overview

##### Design and implement a simple database to manage student imformation using SQL.
---

### Objectives
- [Create a database schema](#create-a-database-schema)
- [Insert, and Update data](#insert-and-update-data)
- [Query data using basic SQL commands](#query-data-using-basic-sql-commands)
- [Tool used](#tool-used)

---

### Database Requirements:

1.Students table:

- Student ID(primary key)

- Name 

- Email

- Phone Number

- Major

2.Cources table:

- Cources ID(primary key)

- Courses Name

- Credits

3.Enrollment table:

- Student ID(foreign key)

- Courses ID(foreign key)

- Grade
---

### TASKS

### Task 1: Create database schema

Create a new database named "StudentDB" and execute the following SQL commands:

```
CREATE TABLE Students (
  StudentID INT PRIMARY KEY,
  Name VARCHAR(50),
  Email VARCHAR(100),
  PhoneNumber VARCHAR(20),
  Major VARCHAR(50)
);

CREATE TABLE Courses (
  CourseID INT PRIMARY KEY,
  CourseName VARCHAR(100),
  Credits INT
);

CREATE TABLE Enrollment (
  StudentID INT,
  CourseID INT,
  Grade VARCHAR(2),
  FOREIGN KEY (StudentID) REFERENCES Students(StudentID),
  FOREIGN KEY (CourseID) REFERENCES Courses(CourseID)
);
```
---

### Task 2: Insert Data

Insert sample data into each table:

```
INSERT INTO Students (StudentID, Name, Email, PhoneNumber, Major)
VALUES
  (1, 'John Etim', 'john.Etim@gmail.com', '08065879031', 'Computer Science'),
  (2, 'Adedimeji Adeleke', 'Adeleke.adedimeji@yahoo.com', '09178905463', 'Mathematics');

INSERT INTO Courses

 (CourseID, CourseName, Credits)

VALUES
  (1, 'Introduction to Computer science', 3),
  (2, 'Equations', 4);

INSERT INTO Enrollment

 (StudentID, CourseID, Grade)

VALUES
  (1, 1, 'A'),
  (1, 2, 'B'),
  (2, 1, 'B');
```
---

### Task 3: Query Data

Execute the following SQL queries:

 1. Retrieve all students:

```
SELECT * FROM Students;
```

2. Retrieve courses with credits > 3:
```
SELECT * FROM Courses WHERE Credits > 3;
```

3. Retrieve students enrolled in 'Introduction to Computer Science ':
```
SELECT s.* 
FROM Students s 
JOIN Enrollment e ON s.StudentID = e.StudentID 
JOIN Courses c ON e.CourseID = c.CourseID 
WHERE c.CourseName = 'Introduction to Computer Science ';
```
---

### Task 4: Update Data*


1. Update John Etim's email:
```
UPDATE Students 
SET Email = 'john.Etim12@gmail.com' 
WHERE StudentID = 1;
```
---
