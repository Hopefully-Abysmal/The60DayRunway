---
Date Created: 2025-06-06 16:18
Last Updated: 2025-06-06 16:18
tags: 
Index:
  - "[[General Development - Vocabulary List]]"
Topic:
  - "[[Coding Vocabulary]]"
Status: Unweathered
Published: true
Author:
---
# [[DEV - Docstrings]]

## 🔍 Definition  
A **docstring** (documentation string) is a special type of **embedded comment** used to describe the **purpose, behavior, inputs, and outputs** of a function, class, or module.

> Unlike regular comments, docstrings often follow **a structured format** and can be **parsed by documentation tools** like `Javadoc`, `pydoc`, or `Doxygen`.

---

## 🧠 Why Use Docstrings?

- Improve readability for other developers (or your future self)
- Enable automatic documentation generation
- Encourage self-documenting code with standardized structure
- Used by many IDEs and linters for autocompletion and inspection

---

## ✍️ Syntax by Language

### 🐍 Python
```python
def greet(name):
    """
    Greet a person by name.

    Parameters:
        name (str): The name of the person.

    Returns:
        str: A greeting message.
    """
    return f"Hello, {name}!"
````

- Enclosed in triple quotes `""" """`
    
- First line: one-sentence summary (used in introspection tools)
    
- Supports extended descriptions and argument/return annotations
    

---

### ☕ Java (Javadoc)

```java
/**
 * Calculates the sum of two integers.
 *
 * @param a The first number
 * @param b The second number
 * @return The sum of a and b
 */
public int add(int a, int b) {
    return a + b;
}
```

- Uses `/** ... */` syntax
    
- Tags like `@param`, `@return`, `@throws` describe structure
    
- Tools: `javadoc` can turn this into HTML documentation

#### 🧠 General Formats

|Tag|Meaning|
|---|---|
|`@param`|Describe input parameters|
|`@return`|What is returned|
|`@throws`|What exceptions might be thrown|
|`@example`|Usage example|
|`@author`|Author name (for module-level docstrings)|



---

### 🌐 JavaScript (JSDoc)

```javascript
/**
 * Add two numbers together.
 * @param {number} a - First number
 * @param {number} b - Second number
 * @returns {number} Sum of a and b
 */
function add(a, b) {
    return a + b;
}
```

- Structured like Javadoc
    
- Popular for TypeScript and JavaScript projects
    
- Tools: `TypeDoc`, `JSDoc`
    

#### 🧠 General Formats

|Tag|Meaning|
|---|---|
|`@param`|Describe input parameters|
|`@return`|What is returned|
|`@throws`|What exceptions might be thrown|
|`@example`|Usage example|
|`@author`|Author name (for module-level docstrings)|


---

### 🦀 Rust

```rust
/// Adds two numbers together.
///
/// # Examples
///
/// ```
/// let result = add(2, 3);
/// assert_eq!(result, 5);
/// ```
fn add(a: i32, b: i32) -> i32 {
    a + b
}
```

- Uses `///` before functions or items
    
- Markdown-supported comments
    
- `cargo doc` generates rich HTML documentation
    

---

### 🦫 Go

```go
// Add returns the sum of two integers.
func Add(a int, b int) int {
    return a + b
}
```

- Uses `//` single-line comments immediately preceding declarations
    
- The comment **must start with the name** of the item to be recognized by `godoc`
    
- No tags or multiline formatting — concise style preferred
    

---

### 🧱 C# (XML Comments)

```csharp
/// <summary>
/// Adds two integers.
/// </summary>
/// <param name="a">First number</param>
/// <param name="b">Second number</param>
/// <returns>The sum of a and b</returns>
public int Add(int a, int b) {
    return a + b;
}
```

- Uses `///` followed by XML-style tags
    
- Tags: `<summary>`, `<param>`, `<returns>`, `<exception>`
    
- Recognized by Visual Studio and `docfx`
    


---

## ✅ Best Practices

- Use full sentences.
    
- Keep first line short and descriptive.
    
- Always document public-facing code.
    
- Prefer docstrings to regular comments for describing **what** and **why**, not just **how**.
    
- Begin with a **short summary** on the first line
    
- Keep docstrings **concise and relevant**
    
- Follow consistent **style guide** for your language (e.g., PEP 257, Javadoc, XML comments)
    
- Use structured tags or formatting **only when needed**
    


---

## 🔁 Related Concepts

- [[DEV - comment]]
    
- [[DEV - function]]
    
- [[DEV - module]]
    
- [[DEV - API]]
    
- [[DEV - IDE]]
    
