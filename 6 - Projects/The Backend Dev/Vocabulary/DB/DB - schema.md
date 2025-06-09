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
  - "[[ChatGPT]]"
aliases:
  - schema
  - database schema
  - data structure
  - table structure
  - relational schema
---
# [[DB - schema]]

## 🔍 Definition  
A **schema** is the formal structure of a database that defines how data is organized—what tables exist, what columns they contain, and how those elements relate to one another.

> In essence: a schema is the blueprint or layout of your database.

---

## 🧠 Key Points  
- Describes the names, types, and relationships of [[DB - table|tables]], [[DB - column|columns]], [[DB - primary key|keys]], and [[DB - constraint|constraints]].
- Can exist at different levels: per-database ([[DB - global|global]]) or per-user ([[DB - namespace|namespace]]).
- Schemas help enforce [[DB - data integrity|data integrity]], [[DB - type safety|type safety]], and [[DB - structure|structure]].
- Used by [[DB - ORM|ORMs]], [[DB - migration|migrations]], and tools like [[DB - Supabase|Supabase]] to auto-generate logic.

---

## ✅ Examples

```sql
-- Define a simple schema via table creation
CREATE TABLE posts (
  id SERIAL PRIMARY KEY,
  title TEXT NOT NULL,
  body TEXT,
  author_id INTEGER REFERENCES users(id)
);

-- In PostgreSQL, create a new schema namespace
CREATE SCHEMA analytics;
````

> Some systems (like [[|PostgreSQL]]) allow multiple schemas within one database for modular organization.

---

## 📚 Real-World Use Cases

- Used when designing or refactoring an app’s data model.
    
- Helps maintain clarity and consistency across teams and queries.
    
- Common in projects using tools like [[DB - Supabase|Supabase]], [[DB - Prisma|Prisma]], [[DB - Rails|Rails]], [[DB - Django|Django]], and enterprise [[DB - RDBMS|RDBMS]].
    

---

## 🧩 Related Concepts

- [[DB - table]]
    
- [[DB - column]]
    
- [[DB - relationship]]
    

---

## Next Concept

#️⃣ [[DB - primary key]]

---

```

Ready to move on to `DB - primary key`?
```