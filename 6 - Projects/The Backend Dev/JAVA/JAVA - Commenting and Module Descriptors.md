## 🗯️ Java Commenting

Java supports **three types of comments**:

|Syntax|Type|Use Case|
|---|---|---|
|`// line comment`|Single-line|Quick notes, disable lines, TODOs|
|`/* ... */`|Multi-line|Longer descriptions or blocks of comments|
|`/** ... */`|Javadoc comment|For API-style documentation on classes/methods|

### 💬 Examples:

```java
// Single-line comment

/*
   This is a multi-line comment
   used for explaining things in detail.
*/

/**
 * Javadoc Comment
 * Describes class/methods for external docs.
 * @author Landon
 * @version 1.0
 */
public class MyModule { ... }
```

---

## 📦 Java Modules (Java 9+)

If you're working in a **modular project**, you’ll need a `module-info.java` file.

### 🔧 What it does:

Defines a module, its **exports**, and **dependencies**.

> It’s the Java equivalent of `package.json`, `Cargo.toml`, or `pyproject.toml` in spirit.

---

## 📄 `module-info.java` — Structure

```java
module my.module.name {
    exports com.mypackage.api;            // Allow others to use this
    requires some.other.module;           // Dependency on another module
}
```

- `exports` → What this module **makes available**
    
- `requires` → What this module **depends on**
    

---

## 🗂️ Where does it go?

It lives at the **root of the source folder** of your module.

```
project-root/
└── src/
    └── my.module.name/
        ├── module-info.java
        └── com/
            └── mypackage/
                └── MyClass.java
```

---

## 🛠 When do I need it?

- **Required**: If you're using **Java Modules** (Jigsaw system, Java 9+).
    
- **Optional**: For small/local apps, you can skip it until you need advanced packaging or visibility control.
    

---

## 🧠 TL;DR

```java
// Single-line
/* Multi-line */
/**
 * Javadoc-style for documentation
 */

// module-info.java (if using modules)
module com.elryan.example {
    exports com.elryan.api;
    requires java.logging;
}
```

Want to see how to structure a simple module-based project or need help adding one to an existing project?

