## **🧱 Foundations: What is a Database?**

1. **[[DB - database]]**
    
    > **A structured collection of data stored electronically. Examples: PostgreSQL, MySQL, MongoDB.**
    
2. **[[DB - table]]**
    
    > **A collection of rows and columns in relational databases (like a spreadsheet).**
    
3. **[[DB - row]]**
    
    > **A single record in a table (e.g. one user).**
    
4. **[[DB - column]]**
    
    > **A field or attribute shared across all rows (e.g. `email`, `age`).**
    
5. **[[DB - schema]]**
    
    > **The structure or blueprint of your database (tables, fields, types, constraints).**
    
6. **[[DB - global]]**
    
    > **A global schema or configuration is one that spans across multiple schemas or namespaces in a DBMS.**
    
7. **[[DB - namespace]]**
    
    > **A logical container (e.g. a schema in PostgreSQL) for organizing related database objects and avoiding naming collisions.**
    

**---**

## **🔢 Data Modeling**

8. **[[DB - primary key]]**
    
    > **A unique identifier for each row (e.g. `user_id`).**
    
9. **[[DB - foreign key]]**
    
    > **A reference to a primary key in another table (used to link data).**
    
10. **[[DB - data type]]**
    
    > **Each column has a type (e.g. `text`, `integer`, `timestamp`).**
    
11. **[[DB - constraint]]**
    
    > **Rules on a column (e.g. `NOT NULL`, `UNIQUE`, `DEFAULT`).**
    
12. **[[DB - relationship]]**
    
    > **How tables connect (one-to-many, many-to-many).**
    
13. **[[DB - structure]]**
    
    > **The organizational layout of data: how tables, fields, and types are arranged in a schema.**
    
14. **[[DB - data integrity]]**
    
    > **The accuracy, consistency, and reliability of data stored in the database across its lifecycle.**
    
15. **[[DB - type safety]]**
    
    > **Ensures that values stored in columns conform to their declared types, preventing runtime errors.**
    

**---**

## **🎯 Querying & Usage**

16. **[[DB - query]]**
    
    > **A command to interact with the database (`SELECT`, `INSERT`, `UPDATE`, `DELETE`).**
    
17. **[[DB - SQL]]**
    
    > **Structured Query Language, used to write queries in relational databases.**
    
18. **[[DB - CRUD]]**
    
    > **Create, Read, Update, Delete — the 4 basic DB operations.**
    
19. **[[DB - filter]]**
    
    > **Use `WHERE` to select only rows that match a condition.**
    
20. **[[DB - join]]**
    
    > **Combine rows from two or more tables based on related columns.**
    

**---**

## **🧰 Tools & Automation**

21. **[[DB - migration]]**
    
    > **A saved schema change (like a Git commit) that updates the database.**
    
22. **[[DB - seed data]]**
    
    > **Initial mock or default data loaded into the DB.**
    
23. **[[DB - view]]**
    
    > **A virtual table built from a query — like a saved `SELECT`.**
    
24. **[[DB - index]]**
    
    > **Speeds up search queries on specific columns.**
    
25. **[[DB - transaction]]**
    
    > **A group of operations treated as one unit — either all succeed or none do.**
    

**---**

## **🧪 TypeScript + Supabase**

26. **[[DB - Supabase]]**
    
    > **A backend-as-a-service platform that wraps PostgreSQL with realtime, auth, storage, and auto-generated APIs.**
    
27. **[[DB - Supabase migration]]**
    
    > **Use `supabase db push` to apply local changes.**
    
28. **[[DB - Supabase types]]**
    
    > **Use `supabase gen types` to generate a `Database` TypeScript type.**
    
29. **[[DB - Supabase client]]**
    
    > **`createClient<Database>(...)` lets you query with type safety.**
    
30. **[[DB - Supabase view]]**
    
    > **A queryable virtual table in Supabase (must also be defined in the `Database` type).**
    

**---**

## **🧭 Parallel Concepts**

- **[[DB - ORM]] → Tools like Prisma, Drizzle, TypeORM**
    
- **[[DB - Prisma]] → A type-safe Node.js ORM for SQL databases**
    
- **[[DB - Rails]] → Ruby on Rails, a full-stack framework with built-in ActiveRecord ORM**
    
- **[[DB - Django]] → A Python web framework with its own ORM system**
    
- **[[DB - RDBMS]] → Relational Database Management System, e.g. PostgreSQL, MySQL**
    
- **[[DB - NoSQL]] → Document-based (e.g. MongoDB), not table-based**
    
- **[[DB - Realtime database]] → Like Firebase, triggers updates on data changes**


**---**

## 🔒 **Security, Architecture, & Reliability**

- [[DB - access control]] → Governs who can see or manipulate which data.
    
- [[DB - multi tenancy]] → Architecture for supporting multiple clients or orgs in one DB instance.
    
- [[DB - modular design]] → Separation of concerns through schemas, namespaces, and clean data modeling.
    
- [[DB - validations]] → Rules (often app-level) for checking data before DB insertion.
    
- [[DB - auditability]] → Ability to track changes, authorship, and data history.
    
- [[DB - corruption]] → Occurs when data is unreadable, incomplete, or altered unexpectedly.
    
- [[DB - duplication]] → The unintentional repetition of records or values.
    
- [[DB - misleading data]] → Valid-looking but incorrect or inconsistent values that distort queries or analysis.

---

**Glossed over concept:**

[[DB - robustness]]
[[DB - performance]]
[[DB - query correctness]]
[[DB - map DB types to programming language types]]
[[DB - structured type]]
[[DB - composite type]]
