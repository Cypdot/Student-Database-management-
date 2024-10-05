# LITA_CLASS_Document

### Project Title: Student Database Management
---

### Project Overview

##### Design and implement a simple database to manage student imformation using SQL.
---

### Objectives
- Create a database schema
- Insert, Update, and delect data
- Query data using basic SQL commands
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

### Task 2: Insert Data

Insert sample data into each table:

 
