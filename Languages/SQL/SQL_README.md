# 🗄️ SQL

> A complete record of my SQL learning journey, focused on relational databases, querying, data manipulation, database design, and cybersecurity applications.

SQL (Structured Query Language) is the standard language used to interact with relational databases. Learning SQL gave me a foundation for understanding how applications store, retrieve, modify, and protect structured data.

SQL is especially important in cybersecurity because many web applications and backend systems rely on databases.

---

## 🎯 Learning Objectives

My SQL learning focused on:

- Understanding relational databases
- Creating and managing database structures
- Writing SQL queries
- Retrieving and filtering data
- Inserting, updating, and deleting data
- Combining data from multiple tables
- Understanding relationships between tables
- Applying constraints
- Understanding database security
- Understanding SQL injection concepts
- Writing safer database queries

---

# 1. 🧩 Database Fundamentals

### What is a Database?

A database is an organized collection of data that can be stored, accessed, managed, and updated efficiently.

### What is a Relational Database?

A relational database stores data in tables consisting of:

```text
Database
   │
   ├── Tables
   │     ├── Rows
   │     └── Columns
   │
   └── Relationships
```

Examples of relational database systems:

- MySQL
- PostgreSQL
- SQLite
- Microsoft SQL Server
- Oracle Database

---

# 2. 📊 Tables, Rows & Columns

A table organizes related information.

Example:

| id | username | role |
|---:|---|---|
| 1 | rudra | student |
| 2 | user2 | admin |

### Concepts

- Table
- Row / Record
- Column / Field
- Data type
- Schema

---

# 3. 🔢 SQL Data Types

Common relational database data types include:

### Numeric

```text
INTEGER
SMALLINT
BIGINT
DECIMAL
FLOAT
```

### String

```text
CHAR
VARCHAR
TEXT
```

### Date & Time

```text
DATE
TIME
TIMESTAMP
```

### Other

```text
BOOLEAN
BLOB
```

Exact data types vary between database systems.

---

# 4. 🏗️ Database & Table Creation

Studied Data Definition Language (DDL).

Common commands:

```sql
CREATE DATABASE database_name;
CREATE TABLE users (
    id INTEGER,
    username VARCHAR(50)
);
```

Also studied:

```sql
ALTER
DROP
TRUNCATE
```

---

# 5. 🔍 SELECT

`SELECT` retrieves data from a table.

Example:

```sql
SELECT * FROM users;
```

Selecting specific columns:

```sql
SELECT username, role
FROM users;
```

---

# 6. 🎯 WHERE

`WHERE` filters records based on a condition.

```sql
SELECT *
FROM users
WHERE role = 'admin';
```

Studied operators:

```text
=
!=
<>
>
<
>=
<=
```

---

# 7. 🧠 Logical Operators

Studied:

```text
AND
OR
NOT
```

Example:

```sql
SELECT *
FROM users
WHERE role = 'admin'
AND id > 10;
```

---

# 8. 🔎 Pattern Matching

Used `LIKE` for pattern matching.

```sql
SELECT *
FROM users
WHERE username LIKE 'rud%';
```

Wildcards:

```text
%   Multiple characters
_   Single character
```

---

# 9. 📑 Sorting

Used `ORDER BY` to sort results.

```sql
SELECT *
FROM users
ORDER BY username ASC;
```

Descending:

```sql
ORDER BY username DESC;
```

---

# 10. 📄 Limiting Results

Used:

```sql
LIMIT
```

Example:

```sql
SELECT *
FROM users
LIMIT 10;
```

Syntax may differ across database systems.

---

# 11. ➕ INSERT

`INSERT` adds new records.

```sql
INSERT INTO users (username, role)
VALUES ('rudra', 'student');
```

Studied:

- Single-row insertion
- Multiple-row insertion
- Column selection

---

# 12. ✏️ UPDATE

`UPDATE` modifies existing records.

```sql
UPDATE users
SET role = 'admin'
WHERE id = 1;
```

### Important

An `UPDATE` without a proper `WHERE` condition can modify many or all records.

---

# 13. 🗑️ DELETE

`DELETE` removes records.

```sql
DELETE FROM users
WHERE id = 1;
```

A missing `WHERE` clause can delete all rows from a table.

---

# 14. 🔗 Primary Keys

A primary key uniquely identifies each row.

Example:

```sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    username VARCHAR(50)
);
```

Properties:

- Unique
- Identifies records
- Cannot contain `NULL` in standard relational usage

---

# 15. 🔗 Foreign Keys

A foreign key creates a relationship between tables.

Example:

```sql
CREATE TABLE orders (
    id INTEGER PRIMARY KEY,
    user_id INTEGER,
    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

Foreign keys help maintain referential integrity.

---

# 16. 🔒 Constraints

Studied common constraints:

```text
PRIMARY KEY
FOREIGN KEY
UNIQUE
NOT NULL
CHECK
DEFAULT
```

Example:

```sql
username VARCHAR(50) NOT NULL UNIQUE
```

Constraints help maintain data quality and integrity.

---

# 17. 🔀 SQL JOINs

JOINs combine related data from multiple tables.

### INNER JOIN

Returns matching records.

```sql
SELECT users.username, orders.id
FROM users
INNER JOIN orders
ON users.id = orders.user_id;
```

### LEFT JOIN

Returns all rows from the left table and matching rows from the right table.

### RIGHT JOIN

Returns all rows from the right table and matching rows from the left table where supported.

### FULL OUTER JOIN

Returns matching and non-matching rows from both sides where supported.

---

# 18. 📊 Aggregate Functions

Studied:

```text
COUNT()
SUM()
AVG()
MIN()
MAX()
```

Example:

```sql
SELECT COUNT(*)
FROM users;
```

Useful for:

- Reporting
- Data analysis
- Statistics
- Monitoring

---

# 19. 📦 GROUP BY

`GROUP BY` groups rows for aggregate calculations.

Example:

```sql
SELECT role, COUNT(*)
FROM users
GROUP BY role;
```

---

# 20. 🎯 HAVING

`HAVING` filters grouped results.

Example:

```sql
SELECT role, COUNT(*)
FROM users
GROUP BY role
HAVING COUNT(*) > 5;
```

---

# 21. 🧩 Subqueries

A subquery is a query inside another query.

Example:

```sql
SELECT username
FROM users
WHERE id IN (
    SELECT user_id
    FROM orders
);
```

Subqueries are useful for complex filtering and data analysis.

---

# 22. 🧠 NULL

`NULL` represents missing or unknown data.

Important:

```sql
IS NULL
IS NOT NULL
```

Example:

```sql
SELECT *
FROM users
WHERE email IS NULL;
```

`NULL` should not normally be compared using `=`.

---

# 23. 🪟 SQL Views

A view is a virtual table based on a query.

Example:

```sql
CREATE VIEW active_users AS
SELECT username
FROM users
WHERE active = TRUE;
```

Views can simplify complex queries and help control what data users access.

---

# 24. ⚡ Indexes

Indexes improve data retrieval performance.

Example:

```sql
CREATE INDEX idx_username
ON users(username);
```

Important trade-off:

```text
Faster reads
     ↕
Additional storage + write overhead
```

Indexes should be designed according to query patterns.

---

# 25. 🔄 Transactions

A transaction groups database operations into a logical unit.

Common commands:

```sql
BEGIN;
COMMIT;
ROLLBACK;
```

### ACID Properties

```text
A — Atomicity
C — Consistency
I — Isolation
D — Durability
```

Transactions help maintain database consistency during multi-step operations.

---

# 26. 🔐 Database Security

Database security includes:

- Authentication
- Authorization
- Access control
- Least privilege
- Encryption
- Auditing
- Logging
- Backup and recovery
- Secure configuration
- Patch management

---

# 27. 👤 Users & Privileges

Database systems commonly support users, roles, and privileges.

Security principles:

```text
User
  ↓
Role
  ↓
Privileges
  ↓
Database Objects
```

Important principle:

> Give users only the permissions they actually need.

This is the **principle of least privilege**.

---

# 28. 🛡️ SQL Injection

SQL injection occurs when untrusted input is improperly incorporated into SQL statements.

Conceptually:

```text
User Input
    ↓
Application
    ↓
Unsafe SQL Construction
    ↓
Database
```

Potential impact can include:

- Unauthorized data access
- Data modification
- Authentication bypass
- Database manipulation

SQL injection testing must only be performed against systems where explicit authorization exists.

---

# 29. 🔒 Preventing SQL Injection

Important defensive practices:

### Parameterized Queries

Use prepared statements instead of constructing SQL from untrusted strings.

Concept:

```text
User Input
    ↓
Parameterized Query
    ↓
Database
```

Also use:

- Input validation
- Least-privilege database accounts
- Safe ORM/database APIs
- Secure error handling
- Proper authentication and authorization

Escaping alone should not be treated as the primary defense when parameterized queries are available.

---

# 30. 🌐 SQL & Web Applications

Many web applications follow a structure similar to:

```text
User
 ↓
Frontend
 ↓
Backend Application
 ↓
SQL Query
 ↓
Database
```

Understanding SQL helps explain:

- Login systems
- User accounts
- Product databases
- Application data
- Session-related data
- Backend APIs
- Web application vulnerabilities

---

# 31. 🔎 SQL in Web Security

SQL knowledge is useful for understanding:

- SQL injection
- Authentication logic
- Database access controls
- Data exposure
- Backend application behavior
- Query construction
- Secure database interaction

It also helps when analyzing web applications during authorized security testing.

---

# 32. 🧪 Practical SQL Workflow

A typical learning workflow:

```text
Create Database
      ↓
Create Tables
      ↓
Define Relationships
      ↓
Insert Data
      ↓
Query Data
      ↓
Filter / Sort
      ↓
Join Tables
      ↓
Aggregate Data
      ↓
Update / Delete
      ↓
Secure the Database
```

---

# 33. 🛠️ SQL Tools & Environments

SQL can be practiced using:

- MySQL
- PostgreSQL
- SQLite
- SQL Server
- Oracle Database
- Database GUI clients
- Command-line database clients

The exact syntax can differ between database systems.

---

# 34. 📚 SQL Command Reference

| Category | Commands / Concepts |
|---|---|
| Database | `CREATE DATABASE`, `DROP DATABASE` |
| Tables | `CREATE TABLE`, `ALTER`, `DROP` |
| Read | `SELECT` |
| Filter | `WHERE` |
| Sort | `ORDER BY` |
| Group | `GROUP BY`, `HAVING` |
| Insert | `INSERT` |
| Update | `UPDATE` |
| Delete | `DELETE` |
| Combine | `JOIN` |
| Aggregate | `COUNT`, `SUM`, `AVG`, `MIN`, `MAX` |
| Constraints | `PRIMARY KEY`, `FOREIGN KEY`, `UNIQUE`, `NOT NULL` |
| Transactions | `BEGIN`, `COMMIT`, `ROLLBACK` |
| Performance | `INDEX` |
| Abstraction | `VIEW` |

---

# 35. 🧠 Key Takeaways

After completing SQL, I understand:

1. How relational databases work
2. How tables, rows, and columns represent data
3. How to create and modify database structures
4. How to retrieve and filter information
5. How to insert, update, and delete records
6. How tables are related using keys
7. How JOINs combine related data
8. How aggregation and grouping work
9. How transactions maintain consistency
10. How indexes affect database performance
11. How database permissions and roles work
12. Why least privilege matters
13. How SQL injection works conceptually
14. How parameterized queries help prevent SQL injection
15. How SQL fits into modern web applications

---

# 🔗 SQL in My Cybersecurity Workflow

SQL fits into my broader cybersecurity learning path:

```text
Programming
    ↓
SQL
    ↓
Databases
    ↓
Web Applications
    ↓
Authentication & Data
    ↓
Web Security
    ↓
SQL Injection Concepts
    ↓
Secure Database Practices
```

---

# ⚖️ Ethical Use

SQL knowledge documented here is intended for:

- Education
- Personal databases
- Authorized security testing
- CTFs
- Intentionally vulnerable applications
- Secure software development
- Defensive security research

I do not use SQL injection techniques or database access methods against systems without explicit authorization.

---

# 📊 Completion Status

| Area | Status |
|---|---|
| Database Fundamentals | ✅ Completed |
| SQL Syntax | ✅ Completed |
| DDL | ✅ Completed |
| DML | ✅ Completed |
| SELECT & Filtering | ✅ Completed |
| Sorting & Grouping | ✅ Completed |
| JOINs | ✅ Completed |
| Aggregate Functions | ✅ Completed |
| Subqueries | ✅ Completed |
| Keys & Constraints | ✅ Completed |
| Views | ✅ Completed |
| Indexes | ✅ Completed |
| Transactions | ✅ Completed |
| Database Security | ✅ Completed |
| SQL Injection Concepts | ✅ Completed |
| Secure Query Practices | ✅ Completed |

---

## 🎯 Next Step

SQL is complete as a foundational database and cybersecurity skill.

The next goal is to apply SQL knowledge through:

- Database projects
- Web application labs
- Secure backend development
- CTFs
- SQL injection labs in authorized environments
- Database security practice

---

## ✅ Status

**SQL — Completed ✅**

SQL is now part of my programming, database, and web-security foundation.

---

### 🗄️ Learn → Query → Analyze → Secure → Build
