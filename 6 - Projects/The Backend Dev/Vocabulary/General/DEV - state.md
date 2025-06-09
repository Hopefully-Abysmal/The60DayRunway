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
---


# 🔹 [[DEV - state]]

## 🔍 Definition

**State** refers to the **stored data** or **current values** associated with a program, object, or system at a specific point in time. In object-oriented programming, it typically means the **values of an object's fields** (aka attributes or properties).

> If an object is a character in a game, its _state_ is its current health, position, and inventory.

---

## 🧠 In [[DEV - Object-Oriented Programming|Object-Oriented Programming]] (OOP)

- The **state** of an object is defined by its **non-static fields** (variables inside the object).
    
- Each instance of a class has its **own state**.
    

### Example:

```java
public class LightSwitch {
    boolean isOn; // this is state
}
```

```java
LightSwitch s1 = new LightSwitch();
s1.isOn = true; // the object s1 is now "on"
```

Different objects can have different states:

```java
LightSwitch s2 = new LightSwitch();
s2.isOn = false;
```

---

## 🔁 Related Concepts

- [[DEV - behavior]]
    
- [[JAVA - object]]
    
- [[JAVA - class]]
    
- [[DEV - variable]]
    
- [[DEV - instance]]
    
- [[JAVA - field]]
    

---

Want me to follow with `[[DEV - behavior]]` next?