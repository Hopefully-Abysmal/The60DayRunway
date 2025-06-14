---
Date Created: 2025-06-06 12:30:30
Last Updated: 2025-06-06 12:30:30
tags: 
Index:
  - "[[General Development - Vocabulary List]]"
Topic:
  - "[[Coding Vocabulary]]"
Status: Unweathered
Published: true
Author: 
aliases:
  - primitive type
  - base type
  - builtin type
  - simple type
  - fundamental type
---
---
# [[DEV - primitive type]]

## 🔍 Definition  
A **primitive type** is a basic, built-in data type provided by a programming language. These types represent the most fundamental building blocks of data.

> In essence: primitive types are the core building blocks of all values—fast, memory-efficient, and language-native.

---

## 🧠 Key Points  
- Examples typically include: `int`, `float`, `bool`, `char`, and `string` (or `str`).
- They are **not objects** (in most languages), though some languages wrap them (e.g. Java’s `Integer`, `Boolean`).
- Used for storing simple values—numbers, truth values, single characters, and text.
- Tend to have fixed memory usage and optimized operations.
- Behave differently from [[DEV - non-primitive type|non-primitive]] types (e.g. no methods, value copying rather than reference sharing).

---

## ✅ Examples

```javascript
let x = 5;           // number (primitive)
let isActive = true; // boolean
let name = "Elryan"; // string
````

```python
x = 42         # int
pi = 3.14      # float
is_valid = True  # bool
```

> In many languages, primitive types are passed **by value**, meaning a copy is made rather than a reference.

---

## 📚 Real-World Use Cases

- Used for [[DEV - configuration flags|configuration flags]], [[DEV - numeric values|numeric values]], and [[DEV - string processing|string processing]].
    
- Helps optimize performance and keep code simple where objects aren't necessary.
    
- Frequently used in low-level programming, performance-critical systems, and embedded devices.
    

---

## 🧩 Related Concepts

- [[DEV - type]]
    
- [[DEV - variable]]
    
- [[DEV - non-primitive type]]
    
- [[DEV - casting]]
    

---

## Next Concept

#️⃣ [[DEV - non-primitive type]]

---

```

Let me know when you're ready for `DEV - non-primitive type`, or want to break down how languages treat primitives under the hood (e.g. boxed vs unboxed).
```