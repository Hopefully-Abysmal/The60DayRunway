---
Date Created: 2025-06-09 15:25:18
Last Updated: 2025-06-09 15:25:18
tags:
  - Resource
  - Vocab
Index:
  - "[[Database Management - Vocabulary List]]"
Topic:
  - "[[Coding Vocabulary]]"
Status: Unweathered
Published: true
Author: 
aliases:
  - primary key
  - PK
  - unique identifier
  - row ID
  - record key
---
# [[DB - primary key]]

## 🔍 Definition  
A **primary key** is a column (or set of columns) in a database table that uniquely identifies each row in that table.

> In essence: it’s the unique ID that guarantees every record is distinct.

---

## 🧠 Key Points  
- Must be unique and not null for every row.
- Commonly named `id`, but can be anything meaningful (e.g., `email`).
- Only one primary key is allowed per table.
- Often used in joins and relationships as a reference.

---

## ✅ Examples

```sql
-- Define a primary key during table creation
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT UNIQUE
);

-- Composite primary key (multiple columns)
CREATE TABLE enrollments (
  student_id INT,
  course_id INT,
  PRIMARY KEY (student_id, course_id)
);
````

> [[DB - Composite Keys|Composite keys]] are useful for modeling [[DB - many to many relationships|many-to-many relationships]].

---

## 📚 Real-World Use Cases

- Used when ensuring that no duplicate users, orders, or records exist.
    
- Helps ensure integrity across related tables via foreign key references.
    
- Common in systems like PostgreSQL, MySQL, SQLite, Supabase.
    

---

## 🧩 Related Concepts

- [[DB - foreign key]]
    
- [[DB - row]]
    
- [[DB - constraint]]
    

---

## Next Concept

#️⃣ [[DB - foreign key]]

---
