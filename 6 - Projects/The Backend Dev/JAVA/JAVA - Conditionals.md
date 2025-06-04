## 🧠 What are Conditionals?

Conditionals allow a Java program to **decide** what to execute **based on boolean logic**. This is how your code _reacts_ to input, state, or events.

---

## ✅ The `if`, `else if`, and `else` Structure

```java
if (condition) {
    // code block A
} else if (anotherCondition) {
    // code block B
} else {
    // code block C
}
```

- Only the **first matching condition** runs.
    
- Conditions must evaluate to a **boolean**.
    

---

## 🔀 Comparison Operators

| Operator | Meaning                  | Example (`x = 5`, `y = 10`) |
| -------- | ------------------------ | --------------------------- |
| ==       | Equal to                 | `x == y` → `false`          |
| `!=`     | Not equal to             | `x != y` → `true`           |
| `>`      | Greater than             | `x > y` → `false`           |
| `<`      | Less than                | `x < y` → `true`            |
| `>=`     | Greater than or equal to | `x >= y` → `false`          |
| `<=`     | Less than or equal to    | `x <= y` → `true`           |

---

## 🧩 Logical Operators

| Operator | Meaning     | Example            |
| -------- | ----------- | ------------------ |
| `&&`     | Logical AND | `x > 0 && y > 0`   |
| `!`      | Logical NOT | `!(x > 0)`         |
| \|\|     | Logical OR  | `a > 0 \|\| b > 0` |

---

## 🔁 Nested `if` Statements

```java
if (score > 70) {
    if (score >= 90) {
        System.out.println("Grade: A");
    } else {
        System.out.println("Grade: B");
    }
}
```

> Avoid deep nesting when possible — refactor to use `else if` or helper methods for clarity.

---

## 🧱 `switch` Statement – Advanced Dive

Used for cleanly branching on **discrete, known values** — often better than chained `if-else`.

### 🧪 Basic Syntax:

```java
switch (expression) {
    case value1:
        // block
        break;
    case value2:
        // block
        break;
    default:
        // fallback
}
```

### ✅ Valid Types for `switch` (Java 7+)

- `byte`, `short`, `int`, `char`
    
- `String`
    
- `enum`
    
- Java 14+ preview: **`switch` expressions** (see below)
    

---

### 🧱 Common Pitfalls

- **Missing `break`** causes _fall-through_:
    
    ```java
    switch (x) {
        case 1: System.out.println("One");
        case 2: System.out.println("Two");
    }
    // prints both for x = 1!
    ```
    
- **Use `default`** to catch unmatched cases.
    

---

### 🧪 `switch` on Strings

```java
String role = "admin";

switch (role) {
    case "admin":
        System.out.println("Full access");
        break;
    case "user":
        System.out.println("Limited access");
        break;
    default:
        System.out.println("Unknown role");
}
```

---

### 🆕 `switch` Expressions (Java 14+)

Cleaner syntax, safer defaults, returns a value.

```java
String result = switch (grade) {
    case "A" -> "Excellent";
    case "B" -> "Good";
    case "C" -> "Average";
    default  -> "Unknown";
};
```

> Use this when **assigning values** instead of just running code.

---

## 🪄 Ternary Operator (Shorthand `if-else`)

```java
String status = (score >= 60) ? "Pass" : "Fail";
```

|Part|Meaning|
|---|---|
|`condition`|Must be boolean|
|`?`|Separates the two outcomes|
|`:`|Separates true case from false|

> Useful for compact logic, but avoid nesting ternaries — gets unreadable fast.

---

## 🧠 Real-World Example

```java
public class Eligibility {
    public static void main(String[] args) {
        int age = 17;
        boolean hasLicense = true;

        if (age >= 18 && hasLicense) {
            System.out.println("You can drive.");
        } else if (age >= 18) {
            System.out.println("Get a license first.");
        } else {
            System.out.println("You're too young to drive.");
        }
    }
}
```

---

## 🧼 Best Practices

- Favor `switch` for **known discrete values**.
    
- Keep `if-else` blocks **shallow**.
    
- Extract logic into methods when complexity grows.
    
- Avoid using `==` with `String`; use `.equals()` instead:
    
    ```java
    if (name.equals("Landon")) {...}
    ```
    

---

## ✅ TL;DR Cheatsheet

```java
// Basic if-else
if (condition) {...}
else if (other) {...}
else {...}

// switch-case
switch (value) {
    case A: ...; break;
    default: ...;
}

// switch expression (Java 14+)
String result = switch (grade) {
    case "A" -> "Great";
    default -> "OK";
};

// Ternary
String msg = (x > 5) ? "High" : "Low";
```

---

Would you like next steps to practice this with user input and branching stories (like a text-based adventure), or want to follow with **loops** or **OOP basics**?