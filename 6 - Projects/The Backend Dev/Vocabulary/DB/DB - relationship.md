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
  - relationship
  - table relationship
  - relational mapping
  - foreign key relationship
  - relational link
---
# [[DB - relationship]]

## 🔍 Definition  
A **relationship** in a database describes how two or more tables are connected through keys, enabling structured connections between records.

> In essence: relationships link rows across tables to model real-world associations like users → posts or orders → products.

---

## 🧠 Key Points  
- Most relationships rely on **foreign keys** referencing **primary keys**.
- Relationships enable **normalized** data structures and reduce redundancy.
- They support **joins**, which retrieve related data across tables.

---
## 🔁 Types of Relationships:
#### [[DB - one-to-many relationships]]

> One record in the primary table is associated with multiple records in the foreign table.

- Focus: The **parent** side of the relationship (e.g., User → Posts).
    
- SQL: `users.id` is referenced by many `posts.user_id`.
    

#### [[DB - many-to-one relationships]]

> Many records in one table relate to a single record in another table.

- Focus: The **child** side of the relationship (e.g., Posts → User).
    
- SQL: Each `posts.user_id` refers to one `users.id`.
    

#### [[DB - one-to-one relationships]]

> A row in one table corresponds directly to one row in another.

- Use for unique extensions (e.g., `users → user_profiles`).
    

#### [[DB - many-to-many relationships]]

> Rows in two tables relate to each other in multiple ways.

- Requires a **junction table** (e.g., `enrollments` between `students` and `courses`).

---

## ✅ Examples

```sql
-- One-to-Many: A user can have many posts
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name TEXT NOT NULL
);

CREATE TABLE posts (
  id SERIAL PRIMARY KEY,
  title TEXT NOT NULL,
  user_id INTEGER REFERENCES users(id)
);

-- Many-to-Many: Students enrolled in many courses
CREATE TABLE enrollments (
  student_id INTEGER REFERENCES students(id),
  course_id INTEGER REFERENCES courses(id),
  PRIMARY KEY (student_id, course_id)
);
```

> The `enrollments` table creates a many-to-many relationship between `students` and `courses`.

---

## 📚 Real-World Use Cases

* Used when linking data between logical entities (users ↔ posts, orders ↔ items).

* Helps organize data into reusable, normalized chunks with minimal duplication.

* Fundamental in relational database systems, supported by ORMs like Prisma, Django, and Rails.

---

## 🧩 Related Concepts

* [[DB - foreign key]]

* [[DB - join]]

* [[DB - schema]]

---

## Next Concept

#️⃣ [[DB - structure]]

---
