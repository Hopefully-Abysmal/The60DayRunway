## 🧱 Java's 8 Primitive Data Types

Java primitives are the **lowest-level building blocks** — fast, memory-efficient, and not objects. (denoted by lowercase variable name)

### 🧠 Core Categories

|Type|Size|Example|Description|
|---|---|---|---|
|`byte`|8-bit|`byte b = 127;`|Small integers (-128 to 127)|
|`short`|16-bit|`short s = 30000;`|Medium integers (-32K to 32K)|
|`int`|32-bit|`int x = 123;`|Default for integers|
|`long`|64-bit|`long l = 123L;`|Large integers (add `L` suffix)|
|`float`|32-bit|`float f = 3.14f;`|Decimal (add `f` suffix)|
|`double`|64-bit|`double d = 3.14159;`|Default for decimals|
|`char`|16-bit|`char c = 'A';`|Single Unicode character|
|`boolean`|1-bit*|`boolean b = true;`|`true` or `false`|

*Note: technically 1-bit, but JVM may use 8-bit or more.

---

## 🗝️ Common Usage Tips

- **Use `int`** for most whole numbers unless memory is tight.
    
- **Use `double`** for decimal numbers by default.
    
- **Always wrap characters in single quotes**: `'A'` not `"A"`.
    
- **Booleans** are super simple: `true` or `false`.
    

---

## 🆚 Primitives vs Wrapper Classes

|Primitive|Wrapper Class|
|---|---|
|`int`|`Integer`|
|`double`|`Double`|
|`char`|`Character`|
|`boolean`|`Boolean`|

> Use wrapper classes when you need objects — e.g. in `ArrayList<Integer>` or for null values.

---

## 📦 Example in Action

```java
public class TypesDemo {
    public static void main(String[] args) {
        int score = 42;
        double ratio = 3.14;
        char grade = 'A';
        boolean passed = true;
        long bigNumber = 1_000_000_000L;
        float temp = 36.6f;

        System.out.println("Score: " + score);
        System.out.println("Ratio: " + ratio);
        System.out.println("Grade: " + grade);
        System.out.println("Passed: " + passed);
    }
}
```

---

## 🧠 TL;DR Cheatsheet

```java
int age = 30;
double price = 19.99;
char letter = 'Z';
boolean isOn = false;
float pi = 3.14f;
long distance = 123456789L;
short smallNum = 32000;
byte tiny = 127;
```

Want to go deeper next? I can show how to convert between types (casting), or jump to arrays, objects, or control flow — your call.

---

[[JAVA - Non-primitive Variables]]