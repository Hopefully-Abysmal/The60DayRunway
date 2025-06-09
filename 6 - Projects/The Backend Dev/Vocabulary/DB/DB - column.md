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
  - column
  - field
  - attribute
  - property
  - data column
---
# [[DB - column]]

## 🔍 Definition  
A **column** is a vertical slice in a database table that defines a specific attribute or field shared by all rows in that table.

> In essence: columns are named containers for values of a specific type across all records.

---

## 🧠 Key Points  
- Each column has a name and a data type (e.g. `TEXT`, `INTEGER`, `TIMESTAMP`).
- Defines what kind of data each row in the table can store at that position.
- Can include constraints like `NOT NULL`, `UNIQUE`, or `DEFAULT`.
- Columns determine the structure (schema) of a table.

---

## ✅ Examples

```sql
-- Create a table with three columns
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT UNIQUE
);

-- Add a new column
ALTER TABLE users ADD COLUMN created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP;
````

> Columns act like the **headings** in a spreadsheet, determining what kind of data each row provides for that field.

---

## 📚 Real-World Use Cases

- Used when defining the shape of a data model.
    
- Helps enforce data consistency and expected input types.
    
- Common in modeling structured data like user profiles, inventory items, or logs.
    

---

## 🧩 Related Concepts

- [[DB - row]]
    
- [[DB - table]]
    
- [[DB - data type]]
    

---

## Next Concept

#️⃣ [[DB - schema]]

---
