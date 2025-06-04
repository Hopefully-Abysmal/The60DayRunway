## 📦 What is a Method?

A **method** is a named block of code that performs a task. It allows you to **reuse**, **organize**, and **abstract** logic.

> In other languages: called "functions", but in Java they’re always tied to classes, so we say "methods".

---

## 🧠 Java Method Anatomy

```java
[modifiers] returnType methodName([parameters]) {
    // method body
}
```

### 🧪 Example

```java
public static int add(int a, int b) {
    return a + b;
}
```

|Part|Meaning|
|---|---|
|`public`|Access modifier (visible to all)|
|`static`|Belongs to the class, not an instance|
|`int`|Return type|
|`add`|Method name|
|`(int a, int b)`|Parameters|
|`return`|Sends result back to caller|

---

## 🔂 Calling Methods

### From `main()`:

```java
public class Demo {
    public static void main(String[] args) {
        int result = add(3, 5);
        System.out.println(result);
    }

    public static int add(int x, int y) {
        return x + y;
    }
}
```

---

## 🧰 `void` Methods (no return value)

```java
public static void greet(String name) {
    System.out.println("Hello, " + name);
}
```

- `void` means **doesn’t return anything**
    
- Used for printing, changing state, etc.
    

---

## 🧾 Parameters vs Arguments

|Term|Meaning|
|---|---|
|**Parameter**|Declared in method definition (`int x`)|
|**Argument**|Actual value passed in (`add(3, 5)`)|

---

## 🌀 Method Overloading (Same name, different params)

```java
public static int square(int x) {
    return x * x;
}

public static double square(double x) {
    return x * x;
}
```

- Java chooses based on argument types.
    

---

## 🌐 Static vs Instance Methods

|Type|Example|Called With|
|---|---|---|
|`static`|`public static int sum(...)`|`ClassName.sum(...)`|
|instance|`public int sum(...)`|`obj.sum(...)`|

---

## 🛡️ Access Modifiers (Quick Look)

|Modifier|Visible To|
|---|---|
|`public`|Everywhere|
|`private`|Only inside the class|
|`protected`|Class + package + subclasses|
|(default)|Package-only (no keyword needed)|

---

## 🔁 Recap Example: All-in-One

```java
public class MathUtils {

    public static int multiply(int a, int b) {
        return a * b;
    }

    public static void printWelcome() {
        System.out.println("Welcome to MathUtils!");
    }

    public double divide(double a, double b) {
        return a / b;
    }
}
```

Then use it:

```java
public class Main {
    public static void main(String[] args) {
        MathUtils.printWelcome(); // static call

        int result = MathUtils.multiply(3, 4);
        System.out.println(result);

        MathUtils utils = new MathUtils();  // instance method
        System.out.println(utils.divide(10, 2));
    }
}
```

---

## ✅ TL;DR Syntax Cheatsheet

```java
// Define a method
public static int add(int x, int y) {
    return x + y;
}

// Call it
int result = add(5, 6);
```

---

