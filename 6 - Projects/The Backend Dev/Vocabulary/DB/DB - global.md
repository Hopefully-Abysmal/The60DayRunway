---
Date Created: 2025-06-09 16:22:19
Last Updated: 2025-06-09 16:22:19
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
aliases:
  - global
  - global schema
  - global context
  - global settings
  - system-wide scope
---
# [[DB - global]]

## 🔍 Definition  
A **global** context in a database refers to settings, configurations, or structures that apply system-wide—across all users, schemas, or databases.

> In essence: “global” means shared, top-level, or outside of any one local scope or [[DB - namespace|namespace]].

---

## 🧠 Key Points  
- Global objects or settings are not restricted to a specific schema or user.
- Examples include global configurations, global variables, or global privileges.
- In PostgreSQL, global roles and permissions affect multiple databases.
- Contrast with **[[DB - local|local]]** or **[[DB - namespace|namespaced]]** definitions that are scoped to a schema or user.

---

## ✅ Examples

```sql
-- PostgreSQL: Create a global role (user account)
CREATE ROLE readonly_user WITH LOGIN PASSWORD 'securepassword';

-- Grant global privileges (across all DBs if allowed)
GRANT CONNECT ON DATABASE mydb TO readonly_user;
````

> These operations apply outside the scope of a single schema or table—they affect access or behavior system-wide.

---

## 📚 Real-World Use Cases

- Used when defining cross-database access rules, admin roles, or shared variables.
    
- Helps ensure consistent configuration across multiple teams, projects, or schemas.
    
- Common in enterprise-grade [[DB - RDBMS|RDBMS]] systems like PostgreSQL, Oracle, and SQL Server.
    

---

## 🧩 Related Concepts

- [[DB - namespace]]
    
- [[DB - schema]]
    
- [[DB - role]]
    
- [[DB - local]]
	

---

## Next Concept

#️⃣ [[DB - namespace]]

---
