---
Date Created: "2025-06-06 12:30:30"
Last Updated: "2025-06-06 12:30:30"
tags:
Index:
  - "[[General Lexicon]]"
Topic:
  - "[[General Development - Vocabulary List]]"
Status: Unweathered
Published: true
Author:
---
---

# [[DEV - comment]]

## 🔍 Definition  
A **comment** is a line or block of text in code that is **ignored by the compiler or interpreter**. Comments are used to **document, explain, or disable** parts of code for readability and maintenance.

---

## 🧠 Why Use Comments?

- Explain **why** something is done (not just how)
- Add TODOs or reminders
- Temporarily disable code (comment it out)
- Help others (and future-you) understand the code

---

## ✍️ Syntax by Language

### ✅ Java
```java
// This is a single-line comment

/*
 This is a
 multi-line comment
 */
````

---

### 🐍 Python

```python
# This is a single-line comment

"""
This is a multi-line string
Often used as a docstring if placed at the start of a function/class
"""
```

See [[DEV - Docstrings]] for more information on docstrings!

---

### 🌐 JavaScript

```javascript
// Single-line comment

/*
 Multi-line comment
 Can span multiple lines
 */
```

---

### 💻 C / C++

```c
// This is a single-line comment

/*
   This is a multi-line comment
*/
```

---

### 🐚 Bash / Shell Scripts

```bash
# This is a comment
echo "Hello"  # This part is a comment too
```

> Bash does not support multi-line comments directly. Use `:` or `<<'END' ... END` for workarounds.

---

## ❌ Bad Practice

```java
int x = 10; // declare x
int y = 20; // declare y
int z = x + y; // add x and y
```

> Comments that state the obvious don't help. Better:

```java
int z = x + y; // Total cost including tax
```

---

## 🔁 Related Concepts

- [[DEV - syntax]]
    
- [[DEV - module]]
    
- [[DEV - function]]
    
- [[DEV - debug]]
    
- [[DEV - IDE]]
    

---

# Next Concept

5. [[DEV - variable]]
    
