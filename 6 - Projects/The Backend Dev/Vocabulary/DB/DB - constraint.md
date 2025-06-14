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
  - constraint
  - SQL constraint
  - column constraint
  - data rule
  - field rule
---
# [[DB - constraint]]

## 🔍 Definition  
A **constraint** is a rule applied to a table or column that restricts the kinds of data that can be inserted, updated, or deleted.

> In essence: constraints enforce structure, validity, and relationships within the database.

---

## 🧠 Key Points  
- Help maintain **data integrity** by validating inputs at the database level.
- Common constraints include:
	- `PRIMARY KEY`: uniquely identifies rows.
	- `FOREIGN KEY`: enforces references between tables.
	- `NOT NULL`: ensures values must be provided.
	- `UNIQUE`: prevents duplicate values in a column.
	- `CHECK`: enforces custom logical rules.
	- `DEFAULT`: sets a fallback value if none is provided.
- Constraints are enforced automatically and prevent invalid data from being stored.

> 🧠 **Compared to [[DB - type safety|Type Safety]]**:  
> Type safety ensures **correct data types** (e.g. only numbers in `INTEGER` fields),  
> while constraints enforce **rules on the data itself** (e.g. only positive numbers, no duplicates, etc.).

---

## ✅ Examples

```sql
-- Create a table with constraints
CREATE TABLE employees (
  id SERIAL PRIMARY KEY,
  email TEXT UNIQUE NOT NULL,
  age INT CHECK (age >= 18),
  start_date DATE DEFAULT CURRENT_DATE
);
````

> Here, `email` must be unique and not null, `age` must be at least 18, and `start_date` defaults to the current date.

---

## 📚 Real-World Use Cases

- Used when enforcing required fields (e.g. `NOT NULL` for critical columns).
    
- Helps ensure relational consistency (e.g. `FOREIGN KEY` for valid references).
    
- Common in all major relational database systems and supported by tools like Supabase, Prisma, and Django ORM.
    

---

## 🧩 Related Concepts

- [[DB - data integrity]]
    
- [[DB - data type]]
    
- [[DB - primary key]]
    

---

## Next Concept

#️⃣ [[DB - relationship]]

---
