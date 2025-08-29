Got it 👍
Here are **simple, clear, interview-ready answers** for your questions 👇

---

### **1. What is SQL?**

SQL (Structured Query Language) is a language used to **store, manage, and retrieve data** from a database.

---

### **2. What is a database?**

A database is an **organized collection of data** that allows easy **storage, retrieval, and management** of information.

---

### **3. What are the main types of SQL commands?**

SQL commands are mainly divided into 5 types:

* **DDL** – Data Definition Language (CREATE, ALTER, DROP)
* **DML** – Data Manipulation Language (INSERT, UPDATE, DELETE)
* **DQL** – Data Query Language (SELECT)
* **DCL** – Data Control Language (GRANT, REVOKE)
* **TCL** – Transaction Control Language (COMMIT, ROLLBACK, SAVEPOINT)

---

### **4. What is the difference between CHAR and VARCHAR2 data types?**

* **CHAR** – Fixed length (e.g., CHAR(10) always stores 10 characters, adding spaces if needed).
* **VARCHAR2** – Variable length (e.g., VARCHAR2(10) stores only the actual characters).

---

### **5. What is a primary key?**

A primary key is a **unique identifier** for each record in a table.
👉 It **does not allow NULL values** and **ensures uniqueness**.

---
Here’s the **simple and interview-focused explanation** 👇

---

**6. What is a foreign key?**
👉 A foreign key is a column (or set of columns) in one table that links to the **primary key** of another table.

* It helps maintain **referential integrity** (relationship between tables).

---

**7. What is the purpose of the DEFAULT constraint?**
👉 The **DEFAULT constraint** automatically assigns a value to a column if no value is provided during insertion.

* Example: If `DEFAULT 0` is set, and you don’t insert anything, it will store `0`.

---

**8. What is normalization in databases?**
👉 Normalization is the process of organizing data in a database to reduce **redundancy** and improve **data integrity**.

* Example: Splitting one big table into smaller related tables.

---

**9. What is denormalization, and when is it used?**
👉 Denormalization is the process of combining normalized tables into fewer tables to improve **read performance**.

* It is used in reporting systems or data warehouses where **fast queries** are needed.

---

**10. What is a query in SQL?**
👉 A query is a request to the database to fetch, insert, update, or delete data.

* Example:

```sql
SELECT * FROM employees;
```

(fetches all employee records).

---
Got it 👍 You want **complete but simple interview-ready definitions** for each SQL question. Here’s the refined version:

---

### **11. What are the different operators available in SQL?**

SQL operators are special symbols or keywords used to perform operations on data in queries.

* **Arithmetic Operators** → `+`, `-`, `*`, `/`, `%` (for mathematical calculations)
* **Comparison Operators** → `=`, `!=` / `<>`, `>`, `<`, `>=`, `<=` (for comparing values)
* **Logical Operators** → `AND`, `OR`, `NOT` (for combining conditions)
* **Special Operators** → `BETWEEN`, `LIKE`, `IN`, `IS NULL`, `EXISTS` (for advanced filtering)

---

### **12. What is a view in SQL?**

A **view** is a **virtual table** based on the result of a SQL query.

* It doesn’t store data itself, but shows data from one or more tables.
* It helps simplify complex queries, improve security, and provide a customized way of looking at data.

👉 Example:

```sql
CREATE VIEW employee_salary AS
SELECT name, salary FROM employees WHERE salary > 50000;
```

---

### **13. What is the purpose of the UNIQUE constraint?**

The **UNIQUE constraint** ensures that all values in a column (or set of columns) are **different**.

* Unlike the **PRIMARY KEY**, a table can have multiple UNIQUE constraints.
* It allows `NULL` values (but only one NULL per column).

👉 Example:

```sql
CREATE TABLE students (
   student_id INT UNIQUE,
   email VARCHAR(50) UNIQUE
);
```

---

### **14. What are the different types of joins in SQL?**

SQL **joins** combine rows from two or more tables based on a related column.

* **INNER JOIN** → Returns only matching rows from both tables.
* **LEFT JOIN (LEFT OUTER JOIN)** → Returns all rows from the left table + matching rows from the right.
* **RIGHT JOIN (RIGHT OUTER JOIN)** → Returns all rows from the right table + matching rows from the left.
* **FULL JOIN (FULL OUTER JOIN)** → Returns all rows when there is a match in either table.
* **CROSS JOIN** → Returns all possible combinations (Cartesian product).
* **SELF JOIN** → A table joined with itself.

---

### **15. What is the difference between INNER JOIN and OUTER JOIN?**

* **INNER JOIN** → Returns only rows where there is a match in both tables.
  👉 Example: Only employees that belong to a department.

* **OUTER JOIN** → Returns matching rows + non-matching rows (depending on LEFT, RIGHT, or FULL).
  👉 Example: All employees, even if they don’t belong to any department.

---
Here’s the **complete definition** (in simple + technical English) of each:

---

### **16. What is the purpose of the GROUP BY clause?**

👉 The **GROUP BY** clause in SQL is used to group rows that have the same values in one or more columns. It is mostly used with **aggregate functions** (like COUNT, SUM, AVG, MAX, MIN) to perform operations on each group of data.

**Example:**

```sql
SELECT department, COUNT(*) 
FROM employees 
GROUP BY department;
```

This query counts employees in each department.

---

### **17. What are aggregate functions in SQL?**

👉 **Aggregate functions** perform calculations on a set of values and return a single summarized result. They are mostly used with **GROUP BY**.

**Common aggregate functions:**

* `COUNT()` → Returns the number of rows.
* `SUM()` → Returns the total sum of numeric values.
* `AVG()` → Returns the average value.
* `MAX()` → Returns the maximum value.
* `MIN()` → Returns the minimum value.

**Example:**

```sql
SELECT AVG(salary) FROM employees;
```

This returns the average salary of employees.

---

### **18. What is a subquery?**

👉 A **subquery** is a query inside another query. It is nested in the `WHERE`, `FROM`, or `SELECT` clause. It helps in fetching results from one query that are used in another.

**Example:**

```sql
SELECT name, salary 
FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);
```

This query selects employees whose salary is greater than the average salary.

---

### **19. What is the difference between the WHERE and HAVING clauses?**

👉 Both **WHERE** and **HAVING** are used to filter data, but the difference is:

* **WHERE** → Filters rows **before grouping** (works on individual rows).
* **HAVING** → Filters groups **after GROUP BY** (works on aggregated results).

**Example:**

```sql
-- Using WHERE
SELECT * FROM employees WHERE salary > 50000;

-- Using HAVING
SELECT department, AVG(salary) 
FROM employees 
GROUP BY department 
HAVING AVG(salary) > 50000;
```

Here, `WHERE` filters employees directly, while `HAVING` filters departments based on average salary.

---

### **20. What are indexes, and why are they used?**

👉 An **index** in SQL is a data structure that improves the speed of retrieving rows from a database table. It works like the index of a book (helps to quickly find information instead of scanning the entire table).

* **Purpose:** Makes queries faster, especially `SELECT` queries with `WHERE`, `ORDER BY`, and `JOIN`.
* **Types:**

  * **Primary Index** → Automatically created with Primary Key.
  * **Unique Index** → Ensures no duplicate values.
  * **Composite Index** → Index on multiple columns.
  * **Clustered Index** → Data is physically sorted (one per table).
  * **Non-clustered Index** → Creates a separate lookup table.

**Example:**

```sql
CREATE INDEX idx_emp_name 
ON employees(name);
```

This creates an index on the `name` column for faster searches.

---
Here’s the **complete definition** for your questions (21–25):

---

### **21. What is the difference between DELETE and TRUNCATE commands?**

* **DELETE**:

  * Removes specific rows from a table using a condition (`WHERE`).
  * Logs each row deletion (slower for large data).
  * Can be rolled back (transaction safe).
  * Does **not reset** identity (auto-increment) values.

* **TRUNCATE**:

  * Removes **all rows** from a table (no condition).
  * Much faster (deallocates data pages).
  * Cannot be rolled back in some databases.
  * **Resets identity** (auto-increment) values.

✅ **Conclusion**: Use `DELETE` for selective deletion and `TRUNCATE` for clearing a table fully.

---

### **22. What is the purpose of the SQL ORDER BY clause?**

* `ORDER BY` is used to **sort query results** in ascending (`ASC`) or descending (`DESC`) order based on one or more columns.
* Example:

  ```sql
  SELECT name, salary 
  FROM employees 
  ORDER BY salary DESC;
  ```

  → Returns employees sorted by highest salary first.

---

---

### **25. What are the types of constraints in SQL?**

Constraints are rules applied to table columns to maintain **data integrity**.

Types of Constraints:

1. **NOT NULL** – Ensures a column cannot have NULL values.
2. **UNIQUE** – Ensures all values in a column are unique.
3. **PRIMARY KEY** – Uniquely identifies each row (NOT NULL + UNIQUE).
4. **FOREIGN KEY** – Ensures referential integrity between tables.
5. **CHECK** – Ensures values satisfy a condition (e.g., salary > 0).
6. **DEFAULT** – Assigns a default value if no value is provided.

---

ठीक है 🙂 मैं आपको **Q.23: What are the differences between SQL and NoSQL databases?** बहुत ही **simple और complete** तरीके से समझाता हूँ, ताकि आपको साफ़ समझ आ जाए।

---

## ✅ SQL vs NoSQL Databases

### 🔹 SQL Databases

* **Full Form** → Structured Query Language
* **Data Storage** → Tables (rows & columns)
* **Schema** → Fixed schema (पहले से तय करना पड़ता है कि table में कौन-कौन से columns होंगे)
* **Scalability** → Vertical (server की power बढ़ानी पड़ती है जैसे CPU, RAM)
* **Examples** → MySQL, PostgreSQL, Oracle, SQL Server
* **Best Use Case** → जब data structured हो (जैसे बैंकिंग, student records, e-commerce orders)।

---

### 🔹 NoSQL Databases

* **Full Form** → Not Only SQL
* **Data Storage** → Different formats (JSON, Key-Value, Document, Graph, Column-based)
* **Schema** → Dynamic schema (data flexible होता है, पहले से तय करने की जरूरत नहीं)
* **Scalability** → Horizontal (ज़्यादा servers जोड़कर scale कर सकते हैं)
* **Examples** → MongoDB, Cassandra, Redis, CouchDB
* **Best Use Case** → जब data unstructured या semi-structured हो (जैसे social media data, IoT, real-time analytics)।

---

