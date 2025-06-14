---
Date Created: 2025-06-10 12:38
Last Updated: 2025-06-10 12:38
tags:
  - Resource
Index:
  - "[[Database Management - Vocabulary List]]"
Topic:
  - "[[Coding Vocabulary]]"
Status: Unweathered
Published: true
aliases:
  - type mapping
  - type translation
  - ORM type mapping
  - database-to-language type map
  - data model sync
---
---
# 📘 [[DB - map DB types to programming language types]]

## 🔍 Definition  
To **map database types to programming language types** means to convert SQL column types (like `INTEGER`, `TEXT`) into equivalent types in a given language (like `int`, `string`)—usually handled automatically by an ORM or database client.

> In essence: it’s the translation layer between your database and your application code.

---

## 🧠 Key Points  
- Required for type-safe interaction between databases and typed languages (e.g. TypeScript, Java, Go).
- Handled by ORMs like Prisma, Django, Sequelize, TypeORM, and Supabase's TypeScript client.
- Mapping can be **implicit** (auto-inferred) or **explicit** (manually declared).
- Mismatched mappings can cause runtime errors or silent data bugs.

---

## ✅ Examples

| Database Type | TypeScript / JavaScript | Python (Django) | Rust (SQLx) |
|---------------|--------------------------|------------------|-------------|
| `INTEGER`     | `number`                 | `int`            | `i32`       |
| `TEXT`        | `string`                 | `str`            | `String`    |
| `BOOLEAN`     | `boolean`                | `bool`           | `bool`      |
| `TIMESTAMP`   | `Date`                   | `datetime`       | `chrono::DateTime` |
| `UUID`        | `string`                 | `uuid.UUID`      | `uuid::Uuid`|

---

## 📚 Real-World Use Cases

- Used when generating models in Prisma (`prisma.schema`) or Django (`models.py`).
    
- Helps catch invalid assignments early in statically typed environments.
    
- Common in full-stack applications using typed ORMs, GraphQL, or REST APIs backed by SQL.
    

---

## 🧩 Related Concepts

- [[DB - data type]]
- [[DEV - type]]
- [[DB - ORM]]

---

## Next Concept

#️⃣ [[DB - validations]]

---
