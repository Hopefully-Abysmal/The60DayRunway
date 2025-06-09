Absolutely — here's your **Deep Dive into [[JAVA - class|Classes]] and Objects** in Java ⚔️  
This is _the_ core of Java’s object-oriented model. Master this and everything else builds on top.

---

## 🧱 What is a Class?

A **class** is a **blueprint** for creating objects (instances). It defines:

- **Fields** (variables → the data)
    
- **Methods** (functions → the behavior)
    

### 🧰 Think of it like a template:

```java
public class Dog {
    String name;
    int age;

    void bark() {
        System.out.println(name + " says: Woof!");
    }
}
```

You don’t _run_ a class — you **instantiate it into an object.**

---

## 🧍 What is an Object?

An **object** is a specific instance of a class.

```java
Dog myDog = new Dog();
myDog.name = "Buddy";
myDog.age = 3;
myDog.bark(); // Buddy says: Woof!
```

> One class can produce many objects — like a cookie cutter and cookies.

---

## 🧬 Class Anatomy

```java
public class Person {
    // Fields (attributes)
    String name;
    int age;

    // Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Method (behavior)
    public void introduce() {
        System.out.println("Hi, I’m " + name + " and I’m " + age + " years old.");
    }
}
```

### ✅ `this` keyword

- Refers to **the current object** (e.g., `this.name` = the field, not the parameter)
    

---

## 🏗️ Creating and Using Objects

```java
public class Main {
    public static void main(String[] args) {
        Person p1 = new Person("Landon", 24);
        p1.introduce(); // Hi, I’m Landon and I’m 24 years old.
    }
}
```

---

## 🧱 Constructors

### What is it?

A **special method** with the same name as the class that initializes objects.

### Types:

|Type|Example|
|---|---|
|Default|`public ClassName() {}`|
|Parameterized|`public ClassName(type param) {...}`|

```java
public class Book {
    String title;
    public Book(String t) {
        title = t;
    }
}
```

---

## 🛡️ Access Modifiers

|Modifier|Meaning|
|---|---|
|`public`|Visible everywhere|
|`private`|Only accessible within the class|
|`protected`|Class + package + subclasses|
|_(default)_|Package-private|

**Encapsulation** = Keep fields `private`, expose via `get` / `set` methods.

```java
private int health;

public int getHealth() { return health; }
public void setHealth(int h) { health = h; }
```

---

## 🎭 Class vs Object vs Instance

|Term|What it means|
|---|---|
|`class`|The **template**|
|`object`|A **live version** of that class|
|`instance`|Synonym for "object"|

---

## 🔧 `static` Fields and Methods

- Belong to the **class**, not to any one object
    
- Shared by all instances
    
- Accessed with `ClassName.method()` or `ClassName.field`
    

```java
public class MathUtils {
    public static int add(int x, int y) {
        return x + y;
    }
}

// Usage:
int sum = MathUtils.add(3, 5);
```

> Use `static` when something is **universal**, not per-object (e.g., math functions, constants)

---

## 🔄 Method Overloading

Same method name, **different parameters**.

```java
public void sayHello() {
    System.out.println("Hello!");
}

public void sayHello(String name) {
    System.out.println("Hello, " + name + "!");
}
```

---

## 🧠 Real-World Example: `BankAccount` class

```java
public class BankAccount {
    private String owner;
    private double balance;

    public BankAccount(String owner, double balance) {
        this.owner = owner;
        this.balance = balance;
    }

    public void deposit(double amount) {
        balance += amount;
    }

    public void display() {
        System.out.println(owner + "'s balance: $" + balance);
    }
}
```

```java
BankAccount b = new BankAccount("Elryan", 1000.0);
b.deposit(500);
b.display(); // Elryan's balance: $1500.0
```

---

## ✅ TL;DR Cheatsheet

```java
// Define a class
public class Car {
    String model;
    int year;

    public Car(String m, int y) {
        model = m;
        year = y;
    }

    public void honk() {
        System.out.println(model + " says Beep!");
    }
}

// Create + use
Car c = new Car("Toyota", 2022);
c.honk();
```

---

## 🧠 Want More?

You can now extend into:

- 🔄 `extends` — inheritance
    
- 🧩 abstract classes vs interfaces
    
- ♻️ object arrays (`Person[] people`)
    
- 💾 object serialization (saving/loading)
    
- 📦 packaging multiple classes with imports
    

Want to go next into **inheritance + polymorphism**, **collections**, or tackle a multi-class mini project (like an RPG or card deck manager)?