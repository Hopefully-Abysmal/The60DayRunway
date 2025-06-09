## 🧱 **Foundations: What is a Database?**

1. [[DB - database]]
    
    > A structured collection of data stored electronically. Examples: PostgreSQL, MySQL, MongoDB.
    
2. [[DB - table]]
    
    > A collection of rows and columns in relational databases (like a spreadsheet).
    
3. [[DB - row]]
    
    > A single record in a table (e.g. one user).
    
4. [[DB - column]]
    
    > A field or attribute shared across all rows (e.g. `email`, `age`).
    
5. [[DB - schema]]
    
    > The structure or blueprint of your database (tables, fields, types, constraints).
    

---

## 🔢 **Data Modeling**

6. [[DB - primary key]]
    
    > A unique identifier for each row (e.g. `user_id`).
    
7. [[DB - foreign key]]
    
    > A reference to a primary key in another table (used to link data).
    
8. [[DB - data type]]
    
    > Each column has a type (e.g. `text`, `integer`, `timestamp`).
    
9. [[DB - constraint]]
    
    > Rules on a column (e.g. `NOT NULL`, `UNIQUE`, `DEFAULT`).
    
10. [[DB - relationship]]
    
    > How tables connect (one-to-many, many-to-many).
    

---

## 🎯 **Querying & Usage**

11. [[DB - query]]
    
    > A command to interact with the database (`SELECT`, `INSERT`, `UPDATE`, `DELETE`).
    
12. [[DB - SQL]]
    
    > Structured Query Language, used to write queries in relational databases.
    
13. [[DB - CRUD]]
    
    > Create, Read, Update, Delete — the 4 basic DB operations.
    
14. [[DB - filter]]
    
    > Use `WHERE` to select only rows that match a condition.
    
15. [[DB - join]]
    
    > Combine rows from two or more tables based on related columns.
    

---

## 🧰 **Tools & Automation**

16. [[DB - migration]]
    
    > A saved schema change (like a Git commit) that updates the database.
    
17. [[DB - seed data]]
    
    > Initial mock or default data loaded into the DB.
    
18. [[DB - view]]
    
    > A virtual table built from a query — like a saved `SELECT`.
    
19. [[DB - index]]
    
    > Speeds up search queries on specific columns.
    
20. [[DB - transaction]]
    
    > A group of operations treated as one unit — either all succeed or none do.
    

---

## 🧪 **TypeScript + Supabase**

21. [[DB - Supabase]]
    
    > A backend-as-a-service platform that wraps PostgreSQL with realtime, auth, storage, and auto-generated APIs.
    
22. [[DB - Supabase migration]]
    
    > Use `supabase db push` to apply local changes.
    
23. [[DB - Supabase types]]
    
    > Use `supabase gen types` to generate a `Database` TypeScript type.
    
24. [[DB - Supabase client]]
    
    > `createClient<Database>(...)` lets you query with type safety.
    
25. [[DB - Supabase view]]
    
    > A queryable virtual table in Supabase (must also be defined in the `Database` type).
    

---

## 🧭 **Parallel Concepts**

- [[DB - ORM]] → Tools like Prisma, Drizzle, TypeORM
    
- [[DB - NoSQL]] → Document-based (e.g. MongoDB), not table-based
    
- [[DB - Realtime database]] → Like Firebase, triggers updates on data changes
    

---

Glossed over topics:

[[DB - global]]
[[DB - namespace]]
[[DB - data integrity]]
[[DB - type safety]]
[[DB - structure]]
[[DB - Prisma]] 
[[DB - Rails]]
[[DB - Django]]
[[DB - RDBMS]]

