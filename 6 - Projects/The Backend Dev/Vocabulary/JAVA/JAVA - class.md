---
Date Created: 2025-06-06 12:30:30
Last Updated: 2025-06-06 12:30:30
tags:
  - Resource
Index:
  - "[[General Lexicon]]"
Topic:
  - "[[JAVA - Vocabulary Index]]"
Status: Unweathered
Published: true
Author:
---
---
# [[JAVA - class]]

## 🔍 Definition  
A `class` in Java is a **blueprint** or **template** for creating objects. It defines the structure and behavior (data and methods) that its objects will have.

In Java, **everything revolves around classes** — even the `main()` method must be inside one.

---

## 🧱 Syntax

```java
public class ClassName {
    // fields
    // constructors
    // methods
}
````

---

## 🧪 Example

```java
public class Dog {
    String name;
    int age;

    public void bark() {
        System.out.println(name + " says: Woof!");
    }
}
```

You can then create an instance:

```java
Dog myDog = new Dog();
myDog.name = "Buddy";
myDog.age = 3;
myDog.bark(); // Buddy says: Woof!
```

---

## 🧠 Key Concepts

- A class **does not store data by itself** — objects do.
    
- One class can produce **many objects** (instances).
    
- You can **nest** classes, use **abstract** or **interface** types, and extend classes with `extends`.
    

---

## 🔁 Related Vocabulary

- [[JAVA - object]]
    
- [[JAVA - method]]
    
- [[JAVA - constructor]]
    
- [[JAVA - static]]
    
- [[JAVA - instance]]
    
- [[JAVA - access modifiers]]
    
