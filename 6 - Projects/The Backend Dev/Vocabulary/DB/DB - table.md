---
Date Created: 2025-06-09 15:25:18
Last Updated: 2025-06-09 15:25:18
tags: 
Index:
  - "[[Database Management - Vocabulary List]]"
Topic:
  - "[[Coding Vocabulary]]"
Status: Unweathered
Published: true
Author: 
aliases:
  - table
  - data table
  - sql table
  - relational table
  - database table
  - record set
  - tables
---
# [[DB - table]]

## 🔍 Definition  
A **table** is a structured set of data within a database, organized into rows and columns — each row representing a record, and each column representing a field or attribute.

> In essence: a table is like a spreadsheet that stores records in a relational database.

---

## 🧠 Key Points  
- Each row is a unique entry (record), and each column defines the type of data stored.
- Tables are the primary way data is organized in relational databases.
- Tables can be linked using keys (e.g. [[DB - primary key|primary keys]] and [[DB - foreign key|foreign keys]]).
- Tables enforce structure through [[DB - schema|schemas]] and [[DB - data type|data types]].

---

## ✅ Examples

```sql
-- Creating a users table
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT UNIQUE,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Querying a table
SELECT * FROM users;
````

> Tables often include constraints like `PRIMARY KEY`, `NOT NULL`, or `UNIQUE` to ensure valid and efficient data storage.

---

## 📚 Real-World Use Cases

- Used when modeling entities like users, products, posts, or transactions in applications.
    
- Helps ensure data is cleanly structured and easily queryable.
    
- Common in relational databases like PostgreSQL, MySQL, SQLite.
    

---

## 🧩 Related Concepts

- [[DB - row]]
    
- [[DB - column]]
    
- [[DB - schema]]
    

---

## Next Concept

#️⃣ [[DB - row]]

---