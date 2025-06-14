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
  - data integrity
  - integrity rules
  - database consistency
  - data correctness
---
# [[DB - data integrity]]

## 🔍 Definition  
**Data integrity** refers to the accuracy, consistency, and reliability of data stored in a database over its lifecycle.

> In essence: it ensures that the data remains correct, valid, and trustworthy from input to query to backup.

---

## 🧠 Key Points  
- Maintained through a combination of:
	- **[[DB - constraint|constraint]]** (e.g. `NOT NULL`, `UNIQUE`, `CHECK`)
	- **Keys** (e.g. [[DB - primary key|primary key]], [[DB - foreign key|foreign key]])
	- **Transactions** (ensuring [[DB - atomicity|atomicity]] and [[DB - rollback|rollback]])
	- **Application-level [[DB - validations|validations]]**
- There are multiple types of integrity:
	- **[[DB - entity integrity|Entity integrity]]**: Each row has a unique identifier (primary key).
	- **[[DB - referential integrity|Referential integrity]]**: Foreign keys correctly link related rows.
	- **[[DB - domain integrity|Domain integrity]]**: Columns store values of the right type and format.
- Without integrity, data becomes [[DB - corruption|corrupted]], [[DB - duplication|duplicated]], or [[DB - misleading data|misleading]].

---

## ✅ Examples

```sql
-- Table enforcing data integrity via constraints
CREATE TABLE orders (
  id SERIAL PRIMARY KEY,
  user_id INTEGER NOT NULL REFERENCES users(id),
  quantity INTEGER CHECK (quantity > 0),
  status TEXT NOT NULL DEFAULT 'pending'
);
````

> This ensures all orders are tied to valid users, have positive quantities, and default to a valid state.

---

## 📚 Real-World Use Cases

- Used when building systems that must be trustworthy, [[DB - auditability|auditable]], or mission-critical (e.g. finance, healthcare).
    
- Helps ensure correctness across millions of rows and complex interrelated data.
    
- Enforced at both database and application layers in nearly all structured data systems.
    

---

## 🧩 Related Concepts

- [[DB - constraint]]
    
- [[DB - primary key]]
    
- [[DB - transaction]]
    

---

## Next Concept

#️⃣ [[DB - type safety]]

---
