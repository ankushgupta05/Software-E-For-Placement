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

✅ Would you like me to continue writing **Q16–Q20 in the same full definition style** so you’ll have a **complete set of 20 SQL interview questions**?
