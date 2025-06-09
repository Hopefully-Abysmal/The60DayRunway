---
Date Created: "2025-06-06 13:02:17"
Last Updated: "2025-06-06 13:02:17"
tags:
Index:
  - "[[Object Oriented Programming - Vocabulary List]]"
Topic:
  - "[[Coding Vocabulary]]"
Status: Unweathered
Published: true
Author:
---
---
# 🧭 [[OOP - class]]

## 🔍 Definition

A **class** is a fundamental building block in object-oriented programming. It is a **template** or **blueprint** that defines the **structure** (fields/state) and **behavior** (methods/functions) that its objects will have.

> A class is like a mold; an object is a thing made from that mold.

---

## 🧱 Components of a Class

- **Fields / Attributes**: Variables that hold data (aka _state_)
    
- **Methods / Functions**: Procedures that operate on data (aka _behavior_)
    
- **Constructors**: Special methods used to initialize new objects
    

---

## 🧪 Language-Agnostic Examples

### Python

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        print(self.name + " says: Woof!")
```

### JavaScript

```javascript
class Dog {
    constructor(name) {
        this.name = name;
    }

    bark() {
        console.log(this.name + " says: Woof!");
    }
}
```

> In both cases, `Dog` is a class that defines a `bark()` method and a `name` field.

---

## 🧠 Key Principles

- A class defines **what an object is and what it can do**.
    
- Objects are **instances** of classes.
    
- Classes help organize code and enforce consistency.
    
- Support **encapsulation**, **inheritance**, and **polymorphism**.
    

---

## 🔁 Related Vocabulary

- [[OOP - object]]
    
- [[OOP - constructor]]
    
- [[OOP - method]]
    
- [[OOP - field]]
    
- [[OOP - state]]
    
- [[OOP - behavior]]
    
- [[OOP - encapsulation]]
    

---

Let me know when you're ready to build out the `[[JAVA - class]]` note or want the `[[OOP - object]]` one next.