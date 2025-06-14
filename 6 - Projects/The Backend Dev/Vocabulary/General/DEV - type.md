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
  - "[[ChatGPT]]"
aliases:
  - type
  - variable type
  - type definition
---
---

# 🧠  [[DEV - type]]

## 🔍 Definition  
A **type** defines the kind of value a variable can hold or an expression can evaluate to—such as a number, string, boolean, or object.

> In essence: types are rules that describe the shape, structure, and behavior of data in a program.

---

## 🧠 Key Points  
- Most languages include **primitive types** (e.g. `int`, `float`, `char`, `bool`) and **complex types** (e.g. `array`, `object`, `class`, `function`).
- Can be **static** (declared explicitly, checked at compile time) or **dynamic** (determined at runtime).
- Strongly typed languages (e.g. Rust, TypeScript) enforce more rigid type rules than weakly typed ones (e.g. JavaScript, Python).
- Types improve safety, readability, and tooling (autocomplete, refactoring, error checking).

---

## ✅ Examples

```typescript
let age: number = 25;
let name: string = "Elryan";
let isActive: boolean = true;
````

```python
age = 25        # int
name = "Elryan" # str
is_active = True  # bool
```

> Many languages also support custom types or generics (e.g. `type User = {...}` in TypeScript).

---

## 📚 Real-World Use Cases

- Used when defining variables, function arguments, return values, and class structures.
    
- Helps catch logic bugs, enforce contracts between parts of your code, and optimize performance.
    
- Essential in tools like TypeScript, Java, Rust, and any statically typed language.
    

---

## 🧩 Related Concepts

- [[DEV - primitive type]]
    
- [[DEV - non-primitive type]]
    
- [[DEV - type conversion]]
    
- [[DB - data type]]
    

---

## Next Concept

#️⃣ [[DEV - primitive type]]

---