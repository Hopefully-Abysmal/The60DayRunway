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
---
---
# [[DEV - expression]]

## 🔍 Definition  
An **expression** is any valid combination of **values**, **variables**, **operators**, and **function calls** that evaluates to a **single value**.

> In short: expressions **produce values**, while statements **do things**.

---

## 🧠 Key Characteristics  
- **Always returns a value**
- Can be part of a **larger statement**
- Can be **assigned to a variable**, passed as arguments, or returned from a function

---

## Java
### Misc Examples:
```java
3 + 4           // evaluates to 7
x * 10          // if x = 2, evaluates to 20
"Hello " + name // concatenates strings
````

### Used in a statement

```java
int total = x + y * 2; // full statement using an expression
```

### 🧠 Expressions vs Statements in JAVA

|Feature|Expression|Statement|
|---|---|---|
|Returns?|Yes|Not necessarily|
|Purpose|Computes a value|Performs an action|
|Usage|Can be embedded in statements|Can include expressions|
|Ends with?|No (but can)|Often ends with semicolon `;`|

---
## Python
### Misc Examples:
```python
3 + 4           # evaluates to 7
x * 10          # if x = 2, evaluates to 20
"Hello " + name # string concatenation
len(items)      # function call that returns a value
````

### Used in a statement

```python
total = x + y * 2  # full statement using an expression
print(total)       # expression as argument in function call
```

### 🧠 Expressions vs Statements in Python

|Feature|Expression|Statement|
|---|---|---|
|Returns?|Yes|Not necessarily|
|Purpose|Computes a value|Performs an action|
|Usage|Often inside statements|May wrap or contain expressions|
|Ends with?|No semicolon (newline ends)|Newline usually ends the statement|

---
## 🔁 Related Concepts

- [[DEV - statement]]
    
- [[DEV - variable]]
    
- [[DEV - boolean]]
    
- [[DEV - condition]]
    
- [[DEV - function]]

---

# Next Concept

4. [[DEV - comment]]

---
