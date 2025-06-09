---
Date Created: 2025-06-06 12:30
Last Updated: 2025-06-06 12:30
tags: 
Index:
  - "[[General Lexicon]]"
Topic:
  - "[[General Development - Vocabulary List]]"
Status: Unweathered
Published: true
Author:
---
# 🧭 [[DEV - object-oriented programming]]

## 🔍 Definition

**Object-Oriented Programming (OOP)** is a **programming paradigm** based on the concept of "**objects**," which contain **data** (called _state_) and **methods** (called _behavior_).

In OOP, software is organized around **interacting objects** rather than actions and logic.

---

## 🧱 Core Principles (The “Big Four”)

| Principle                                  | Meaning                                                                               |
| ------------------------------------------ | ------------------------------------------------------------------------------------- |
| **[[OOP - encapsulation\|Encapsulation]]** | Group related data + behavior in one unit; hide internal details from outside use     |
| **Abstraction**                            | Expose only essential features and hide complexity                                    |
| **Inheritance**                            | Let one class derive fields/methods from another (code reuse & hierarchy)             |
| **Polymorphism**                           | Treat different types of objects through a common interface (e.g., method overriding) |

---

## 📦 In Practice

In Java and many other OOP languages:

- A `class` defines a **template** (fields + methods).
    
- An `object` is a **live instance** of that class.
    
- Objects **interact** by calling each other’s methods.
    
- Programs are **built from networks of objects**.
    

---

## 🧪 Example (Java)

```java
public class Dog {
    String name;
    void bark() {
        System.out.println(name + " says: Woof!");
    }
}

Dog d = new Dog();
d.name = "Buddy";
d.bark(); // Buddy says: Woof!
```

- `Dog` = class (blueprint)
    
- `d` = object (instance)
    
- `name` = state
    
- `bark()` = behavior
    

---

## 🎯 Why Use OOP?

- Models real-world systems more naturally
    
- Promotes modularity and reuse
    
- Scales well in large codebases
    

---

## 🔁 Related Vocabulary

- [[DEV - class]]
    
- [[DEV - object]]
    
- [[DEV - state]]
    
- [[DEV - behavior]]
    
- [[DEV - encapsulation]]
    
- [[DEV - inheritance]]
    
- [[DEV - polymorphism]]
    
- [[DEV - abstraction]]
    
- [[JAVA - class]]
    
- [[JAVA - object]]
    

---

Let me know if you'd like entries for the "big four" OOP principles next (encapsulation, abstraction, etc.) — they're perfect bite-sized notes.