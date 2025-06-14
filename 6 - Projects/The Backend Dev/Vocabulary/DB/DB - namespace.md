---
Date Created: 2025-06-09 16:22:19
Last Updated: 2025-06-09 16:22:19
tags: 
Index:
  - "[[Database Management - Vocabulary List]]"
Topic:
  - "[[Coding Vocabulary]]"
Status: Unweathered
Published: true
Author: 
aliases:
  - namespace
  - schema namespace
  - logical namespace
  - DB namespace
  - database context
---
# [[DB - namespace]]

## 🔍 Definition  
A **namespace** in a database is a logical container used to group and isolate objects like tables, views, and functions—preventing naming collisions and organizing data.

> In essence: a namespace is like a labeled folder inside the database that holds its own tables and logic.

---

## 🧠 Key Points  
- In relational databases (like PostgreSQL and Supabase), **[[DB - schema|schemas]] function as namespaces**.
- You can have tables with the same name in different namespaces (e.g. `public.users` vs `admin.users`).
- Namespaces support **[[DB - modular design|modular design]]**, **[[DB - multi tenancy|multi-tenancy]]**, and **[[DB - access control|access control]]**.
- Though often used interchangeably, **"namespace" is a broader concept**:
	- All schemas are namespaces, but not all namespaces are necessarily schemas (especially in other systems like programming languages or document stores).
- The idea of namespaces also appears in software contexts (e.g. Python modules, C++ namespaces).

---

## ✅ Examples

```sql
-- Create a new namespace (schema) in PostgreSQL
CREATE SCHEMA analytics;

-- Create a table within that namespace
CREATE TABLE analytics.metrics (
  id SERIAL PRIMARY KEY,
  page_views INT,
  recorded_at TIMESTAMP
);

-- Query from a specific namespace
SELECT * FROM analytics.metrics;
````

> This separates analytics data from other domains, enabling cleaner architecture and safer operations.

---

## 📚 Real-World Use Cases

- Used when separating different modules, teams, or purposes within one database.
    
- Helps prevent naming conflicts (e.g., multiple `users` tables across apps).
    
- Common in systems like PostgreSQL, Oracle, and Supabase—where schemas act as namespaces.
    

---

## 🧩 Related Concepts

- [[DB - schema]]
    
- [[DB - global]]
    
- [[DB - structure]]
    

---

## Next Concept

#️⃣ [[DB - data integrity]]

---

