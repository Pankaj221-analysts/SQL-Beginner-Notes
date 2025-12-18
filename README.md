📘# SQL Beginner Notes 

These notes are designed for absolute beginners with clear explanations, syntax, and examples.

⸻

📌 What is SQL?

SQL (Structured Query Language) is used to store, retrieve, update, and manage data in relational databases.

Popular Databases:
	•	MySQL
	•	PostgreSQL
	•	Oracle
	•	SQL Server

⸻

📌 SQL Data Types (Basic)

Data Type	Description
INT	Stores whole numbers
VARCHAR(n)	Stores text
DATE	Stores date
FLOAT	Stores decimal values
BOOLEAN	Stores TRUE or FALSE


⸻

📌 CREATE TABLE

Used to create a new table.

CREATE TABLE students (
  id INT,
  name VARCHAR(50),
  age INT,
  city VARCHAR(50)
);


⸻

📌 INSERT INTO

Used to insert data into a table.

INSERT INTO students VALUES (1, 'Rahul', 21, 'Delhi');


⸻

📌 SELECT Statement

Used to fetch data from a table.

SELECT * FROM students;

Select specific columns:

SELECT name, city FROM students;


⸻

📌 WHERE Clause

Used to apply conditions.

SELECT * FROM students WHERE city = 'Delhi';


⸻

📌 DISTINCT

Used to remove duplicate values.

SELECT DISTINCT city FROM students;


⸻

📌 ORDER BY

Used to sort results.

SELECT * FROM students ORDER BY age ASC;

Descending order:

SELECT * FROM students ORDER BY age DESC;


⸻

📌 AND / OR / NOT Operators

SELECT * FROM students WHERE age > 18 AND city = 'Delhi';

SELECT * FROM students WHERE city = 'Delhi' OR city = 'Mumbai';


⸻

📌 Aggregate Functions

Function	Description
COUNT()	Counts rows
SUM()	Adds values
AVG()	Average
MIN()	Minimum
MAX()	Maximum

Example:

SELECT COUNT(*) FROM students;


⸻

📌 GROUP BY

Used with aggregate functions.

SELECT city, COUNT(*) FROM students GROUP BY city;


⸻

📌 HAVING

Used to filter grouped data.

SELECT city, COUNT(*) FROM students GROUP BY city HAVING COUNT(*) > 1;


⸻

📌 JOINS (Basic)

Used to combine data from multiple tables.

INNER JOIN

SELECT students.name, orders.amount
FROM students
INNER JOIN orders
ON students.id = orders.student_id;


⸻

📌 SUBQUERY

Query inside another query.

SELECT name FROM students
WHERE age > (SELECT AVG(age) FROM students);


⸻

📌 CTE (Common Table Expression)

Temporary result set using WITH.

WITH adult_students AS (
  SELECT * FROM students WHERE age >= 18
)
SELECT * FROM adult_students;


⸻

📌 UPDATE

Used to modify existing data.

UPDATE students SET city = 'Mumbai' WHERE id = 1;


⸻

📌 DELETE

Used to remove records.

DELETE FROM students WHERE id = 1;


⸻

📌 TRUNCATE

Deletes all data but keeps table structure.

TRUNCATE TABLE students;


⸻

📌 DROP TABLE

Deletes table completely.

DROP TABLE students;


⸻

📌 SQL Constraints

Constraint	Purpose
PRIMARY KEY	Unique identifier
NOT NULL	Cannot be empty
UNIQUE	Unique value
DEFAULT	Default value
FOREIGN KEY	Links tables

Example:

CREATE TABLE users (
  id INT PRIMARY KEY,
  email VARCHAR(100) UNIQUE
);


⸻

📌 Interview Practice Questions
	1.	What is SQL?
	2.	Difference between DELETE and TRUNCATE?
	3.	What is PRIMARY KEY?
	4.	What is JOIN?
	5.	What is GROUP BY?

⸻

⭐ If you like these notes, don’t forget to give a GitHub Star!# SQL-Beginner-Notes
SQL beginner notes with examples
