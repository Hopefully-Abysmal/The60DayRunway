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
  - row
  - record
  - tuple
  - entry
  - data row
---
# [[DB - row]]

## 🔍 Definition  
A **row** is a single record in a database table, representing one instance of the entity the table stores.

> In essence: each row is a horizontal slice of data that corresponds to one item or object.

---

## 🧠 Key Points  
- Each row contains values for every column in the table.
- Rows are uniquely identified by a [[DB - primary key|primary key]].
- In SQL, a `SELECT` query returns rows from a table.
- Rows represent structured entities like users, posts, or transactions.

---

## ✅ Examples

```sql
-- Insert a row into the users table
INSERT INTO users (name, email) VALUES ('Balthazar', 'balthazar@example.com');

-- Select all rows from a table
SELECT * FROM users;
````

> Each returned line in the query output is a row, mapping directly to one record in the table.

---

## 📚 Real-World Use Cases

- Used when retrieving or modifying a specific entry in a database.
    
- Helps structure data for transactional systems.
    
- Common in any app storing user input, logs, sales, or metadata.
    

---

## 🧩 Related Concepts

- [[DB - column]]
    
- [[DB - table]]
    
- [[DB - primary key]]
    

---

## Next Concept

#️⃣ [[DB - column]]

---
