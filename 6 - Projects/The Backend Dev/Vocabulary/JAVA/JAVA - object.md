---
Date Created: "2025-06-06 12:30:30"
Last Updated: "2025-06-06 12:30:30"
tags:
Index:
  - "[[General Lexicon]]"
Topic:
  - "[[JAVA - Vocabulary Index]]"
Status: Unweathered
Published: true
Author:
---
---
# 🔹 [[JAVA - object]]

## 🔍 Definition

An **object** is a **concrete instance** of a `class`. While a class defines the structure and behavior, an object actually holds the **data** and can perform the **methods** defined in the class.

Each object has:

- Its **own copy** of non-[[JAVA - static|static]] fields ([[DEV - state|state]])
    
- Access to the class’s **methods** (behavior)
    

---

## 🧪 Example

Given the class:

```java
public class Car {
    String model;
    int year;

    void drive() {
        System.out.println(model + " is driving...");
    }
}
```

You can create and use objects like this:

```java
Car myCar = new Car();
myCar.model = "Honda";
myCar.year = 2021;
myCar.drive(); // Output: Honda is driving...
```

---

## 🧠 Notes

- Objects are created using the `new` keyword.
    
- Each object has its own **identity**, **state**, and **behavior**.
    
- Multiple objects from the same class can coexist independently.
    

```java
Car car1 = new Car();
Car car2 = new Car();
```

---

## 📎 Related Vocabulary

- [[JAVA - class]]
    
- [[JAVA - new]]
    
- [[JAVA - instance]]
    
- [[JAVA - constructor]]
    
- [[JAVA - method]]
    

---