## 🧱 Java Program Skeleton

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

| Element                | Meaning                                    |
| ---------------------- | ------------------------------------------ |
| `public class`         | Declares a class (must match filename)     |
| `main(String[] args)`  | Entry point – JVM starts running from here |
| `System.out.println()` | Prints output to console                   |
| Curly braces `{}`      | Define code blocks                         |
| Semicolon `;`          | Ends most statements                       |

---

## 🗂️ Java File = One Public Class

- File **name must match** the **public class** name:
    
    ✅ `HelloWorld.java` → `public class HelloWorld`
    

---

## 🔤 Case Sensitivity

- `Main`, `main`, and `MAIN` are **all different** — Java is case-sensitive.
    

---

## 🔄 Operators

| Type       | Examples          | Purpose                   |
| ---------- | ----------------- | ------------------------- |
| Arithmetic | `+ - * / %`       | Basic math                |
| Comparison | `!= == < > <= >=` | Conditions                |
| Logical    | `&&`              |                           |
| Assignment | `+= = -=`         | Assign & update variables |

---

## 🧠 TL;DR Java Syntax Guide

```java
// Class must match file name
public class MyApp {
    public static void main(String[] args) {
        // Print
        System.out.println("🚀 Java Speedrun");

        // Variables
        int a = 5;
        double b = 3.14;
        char c = 'X';
        boolean d = true;

        // Conditional
        if (a > 3) {
            System.out.println("Greater than 3");
        }

        // Loop
        for (int i = 0; i < 3; i++) {
            System.out.println(i);
        }

        // Function call
        greet("Landon");
    }

    public static void greet(String name) {
        System.out.println("Hello, " + name);
    }
}
```

---

# Relevant Notes:

[[JAVA - Relevant Filetypes]]

[[JAVA - Primitive Variable Types]]
[[JAVA - Non-primitive Variables]]
[[JAVA - Commenting and Module Descriptors]]
[[JAVA - Control Flow]]
[[JAVA - Methods (Functions)]]
