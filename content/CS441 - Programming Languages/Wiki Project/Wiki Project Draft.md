---
title: "Wiki Project Draft"
date: 2022-11-14
---

# Overview

SQL (Structured Query Language) is a declarative programming language designed for interacting with databases.

# History

SQL was introduced in a 1974 paper by recent PhD graduates Donald Chamberlin and Raymond Boyce. Originally named SEQUEL (Structured English Query Language),

# Features



# Example Code

SQL provides mechanisms for defining and altering table schemas, operating as a data *definition* language. Note that the `SERIAL` type creates an automatically-incrementing integer counter, which can be helpful for identifier fields.

```sql
CREATE TABLE employee (
    id 	  		SERIAL 	PRIMARY KEY,
    dept_id 	INT 	NOT NULL,
    name 	  	TEXT 	NOT NULL,
    salary  	INT 	NOT NULL
);

CREATE TABLE department (
    id 			INT 	PRIMARY KEY,
    name 		TEXT
);

ALTER TABLE employee
ADD CONSTRAINT fk_emp_dept
FOREIGN KEY (dept_id)         ; an employee `dept_id` field...
REFERENCES department (id);   ; references a department `id` field.
```

SQL also operates as a data *manipulation* language, allowing you to create, update, or read individual rows in the tables you've created.

```sql
INSERT INTO department (id, name)
VALUES
	(1, 'Retail'),
    (2, 'Operations'),
    (3, 'Sales');
    
INSERT INTO employee (dept_id, name, salary)
VALUES
	(1, 'Alice', 50000),
	(1, 'Bob',   57000),
    (1, 'Carol', 60000),
    (2, 'Dave',  55000),
    (2, 'Eve',   70000),
    (3, 'Frank', 65000),
    (3, 'Grace', 55000);
```

You can use `SELECT` statements to read data from the database. The following query:

```sql
SELECT
	emp.name AS employee_name,
    emp.salary,
    dept.name AS department_name
FROM employee AS emp
	JOIN department AS dept 
    ON emp.dept_id = dept.id
ORDER BY salary DESC;
```

...produces a set of results that looks like this:

| employee_name | salary | department_name |
| ------------- | ------ | --------------- |
| Eve           | 70000  | Operations      |
| Frank         | 65000  | Sales           |
| Carol         | 60000  | Retail          |
| Bob           | 57000  | Retail          |
| Dave          | 55000  | Operations      |
| Grace         | 55000  | Sales           |
| Alice         | 50000  | Retail          |

SQL also supports aggregate functions like `SUM`, `AVG`, and more. For example, to find the average salary per department, we could write a query like the following:

```sql
SELECT dept.name, ROUND(AVG(salary), 0) as avg_salary
FROM employee AS emp
	JOIN department AS dept
	ON emp.dept_id = dept.id
GROUP BY dept.id
ORDER BY avg_salary DESC;
```

| name       | avg_salary |
| ---------- | ---------- |
| Operations | 62500      |
| Sales      | 60000      |
| Retail     | 55667      |

# Summary



# Further Reading

[1]:	Donald D. Chamberlin. 2012. Early History of SQL. IEEE Annals Hist. Comput. 34, 4 (October 2012), 78–82. DOI:https://doi.org/10.1109/MAHC.2012.61
[2]:	Donald D. Chamberlin, Morton M. Astrahan, Michael W. Blasgen, James N. Gray, W. Frank King, Bruce G. Lindsay, Raymond Lorie, James W. Mehl, Thomas G. Price, Franco Putzolu, Patricia Griffiths Selinger, Mario Schkolnick, Donald R. Slutz, Irving L. Traiger, Bradford W. Wade, and Robert A. Yost. 1981. A history and evaluation of System R. Commun. ACM 24, 10 (October 1981), 632–646. DOI:https://doi.org/10.1145/358769.358784
[3]:	Donald D. Chamberlin and Raymond F. Boyce. 1974. SEQUEL: A structured English query language. In Proceedings of the 1974 ACM SIGFIDET (now SIGMOD) workshop on Data description, access and control (SIGFIDET ’74), Association for Computing Machinery, New York, NY, USA, 249–264. DOI:https://doi.org/10.1145/800296.811515
[4]:	E. F. Codd. 1970. A relational model of data for large shared data banks. Commun. ACM 13, 6 (June 1970), 377–387. DOI:https://doi.org/10.1145/362384.362685
[5]:	2022. SQL. Wikipedia. Retrieved October 31, 2022 from https://en.wikipedia.org/w/index.php?title=SQL&oldid=1119270475