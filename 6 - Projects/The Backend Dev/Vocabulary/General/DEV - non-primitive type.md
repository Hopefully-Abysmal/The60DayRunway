---
Date Created: 2025-06-06 12:30:30
Last Updated: 2025-06-06 12:30:30
tags: 
Index:
  - "[[General Lexicon]]"
Topic:
  - "[[General Development - Vocabulary List]]"
Status: Unweathered
Published: true
Author: 
aliases:
  - non-primitive type
---
---

# [[DEV - non-primitive type]]

## 🔍 Definition  
A **non-primitive type** is a complex data structure made up of one or more primitive types. These types can store multiple values, define behavior, or represent real-world entities.

> In essence: non-primitive types are built from primitives and used to structure or encapsulate data more meaningfully.

---

## 🧠 Key Points  
- Often implemented as **[[DEV - reference type|reference types]]**, because they are usually passed by reference (not by value). However, not all non-primitives are reference types in every language.
- Examples include: [[DEV - array|arrays]], [[DEV - list|lists]], [[DEV - map|maps]], [[DEV - object|objects]], [[DEV - function|functions]], [[DEV - class|classes]], [[DEV - struct|structs]].
- Can contain other non-primitive or primitive types.
- Typically **[[DEV - mutable|mutable]]** (can be changed after creation), though this depends on the language.
- Used to model:
	- [[DEV - nested data| Nested Data]] → Hierarchical data (e.g. JSON, trees)
	- [[DEV - reusable logic| Reusable Logic]] → Functions, modules, DRY principle
	- [[DEV - complex behavior| Complex Behavior]] → State machines, reactive flows, domain models

---

## ✅ Examples

```javascript
let user = { name: "Elryan", age: 22 };  // object (non-primitive)
let tags = ["dev", "db", "learning"];    // array
````

```python
user = { "name": "Elryan", "age": 22 }   # dict
numbers = [1, 2, 3]                      # list
```

> In most languages, non-primitive types are stored in the **heap** and referenced by **pointers** in variables.

---
### 🧠 **Key Differences between non-primitives:**

| Term                                          | Emphasis                                                       | Example Notes                                            |
| --------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------- |
| **Non-primitive**                             | Anything not built into the language core                      | Arrays, objects, classes — anything user-defined or rich |
| **[[DEV - complex type\|Complex type]]**      | Structure with **multiple sub-values** or **nested structure** | Nested dicts, records, objects with attributes           |
| **[[DB - composite type\|Composite type]]**   | Built by combining multiple fields/types                       | Structs, tuples, classes                                 |
| **[[DEV - reference type\|Reference type]]**  | Stored by reference (i.e. pointer in memory)                   | Objects in JS, classes in Java                           |
| **[[DB - structured type\|Structured type]]** | Has a fixed internal format or schema                          | JSON, protobuf, database records                         |

---
## 📚 Real-World Use Cases

- Used when modeling users, events, collections of data, or business logic.
    
- Helps structure your code for reusability, clarity, and performance.
    
- Essential in object-oriented, functional, and data-centric programming paradigms.
    

---

## 🧩 Related Concepts

- [[DEV - primitive type]]
    
- [[DEV - type]]
    
- [[DEV - array]]
    
- [[DEV - map]]
    
- [[DEV - function]]
    
- [[DEV - class]] 
    

---

## Next Concept

#️⃣ [[DEV - casting]]

---
