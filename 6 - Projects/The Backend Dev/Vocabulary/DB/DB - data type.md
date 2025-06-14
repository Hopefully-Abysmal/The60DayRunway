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
  - "[[ChatGPT]]"
aliases:
  - column type
  - field type
  - SQL type
  - data type
  - datatype
---

# [[DB - data type]]

## 🔍 Definition  
A **data type** defines the kind of value that can be stored in a column—such as text, numbers, dates, or booleans.

> In essence: it sets the rules for what kind of data each column can accept.

---

## 🧠 Key Points  
- Determines the format, storage size, and operations allowed on a column.
- Data types form the foundation of **[[DB - type safety|type safety]]**—they define what kind of values are allowed and prevent invalid inputs (e.g. text in a numeric field).
- Common types include `INTEGER`, `TEXT`, `BOOLEAN`, `DATE`, `TIMESTAMP`, and `UUID`.
- Some types support constraints like length or precision (e.g., `VARCHAR(255)`).
- Strong typing helps enforce correctness and optimize performance.

---

## ✅ Examples

```sql
-- Define data types when creating a table
CREATE TABLE products (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  price NUMERIC(10, 2),
  in_stock BOOLEAN DEFAULT true,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
````

> Choosing the right data type can prevent bugs, save storage space, and improve query speed.

---

## 📚 Real-World Use Cases

- Used when enforcing consistent formats for values (e.g. email as `TEXT`, quantity as `INTEGER`).
    
- Helps ensure data validation and correctness at the database level.
    
- Common in SQL databases, Supabase, Prisma, and ORM schemas.
    

---

## 🧩 Related Concepts

- [[DB - column]]
    
- [[DB - constraint]]
    
- [[DB - type safety]]
    

---

## Next Concept

#️⃣ [[DB - constraint]]

---
