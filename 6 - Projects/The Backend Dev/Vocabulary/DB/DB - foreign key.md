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
  - foreign key
  - FK
  - external reference
  - relational link
  - cross-table key
---

# [[DB - foreign key]]

## 🔍 Definition  
A **foreign key** is a column (or combination of columns) in one table that refers to the primary key of another table, establishing a relationship between the two.

> In essence: it connects rows in one table to corresponding rows in another.

---

## 🧠 Key Points  
- Enforces referential integrity between tables.
- Must match values from the referenced primary key (or be `NULL` if allowed).
- Can be used to model [[DB - one to many relationships|one-to-many]] or [[DB - many to one relationships|many-to-one]] relationships.
- Deleting or updating a row in the parent table can affect related rows if configured (`ON DELETE CASCADE`, etc.).

---

## ✅ Examples

```sql
-- Create two related tables
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL
);

CREATE TABLE posts (
  id SERIAL PRIMARY KEY,
  title TEXT NOT NULL,
  author_id INT,
  FOREIGN KEY (author_id) REFERENCES users(id)
);
````

> The `author_id` in `posts` refers to the `id` in `users`, linking each post to its creator.

---

## 📚 Real-World Use Cases

- Used when modeling relationships like users and posts, orders and customers, or comments and articles.
    
- Helps ensure that related data remains consistent across tables.
    
- Common in normalized [[DB - relational database|relational database]] systems like PostgreSQL, MySQL, and Supabase.
    

---

## 🧩 Related Concepts

- [[DB - primary key]]
    
- [[DB - relationship]]
    
- [[DB - constraint]]
    

---

## Next Concept

#️⃣ [[DB - data type]]

---
