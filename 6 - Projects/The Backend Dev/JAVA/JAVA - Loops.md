## 🔁 What are Loops?

Loops let your program **repeat code** while a condition is true or for a set number of iterations. Great for processing data, automating tasks, or creating flow.

---

## 🧱 Types of Loops in Java

|Loop Type|Use Case|Runs...|
|---|---|---|
|`for`|Count-controlled loops|Known number of times|
|`while`|Condition-controlled|Zero or more times|
|`do...while`|Condition-controlled (post-check)|**At least once**|
|`for-each`|Collection traversal|Each item in a group|

---

## 🔁 1. `for` Loop — _Best for counted repetition_

### Syntax:

```java
for (initialization; condition; update) {
    // loop body
}
```

### Example:

```java
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i);
}
```

### Breakdown:

|Part|Description|
|---|---|
|`int i = 0`|Initialize loop variable|
|`i < 5`|Loop while true|
|`i++`|Increment after each iteration|

✅ Great for **fixed number of steps**  
✅ Used often with arrays via indices

---

## 🔁 2. `while` Loop — _Use when you don’t know how many times_

### Syntax:

```java
while (condition) {
    // code
}
```

### Example:

```java
int count = 0;
while (count < 3) {
    System.out.println(count);
    count++;
}
```

✅ Great for **waiting on conditions**, user input, etc.  
⚠️ Risk of **infinite loops** if condition never becomes false

---

## 🔁 3. `do...while` Loop — _Always runs at least once_

### Syntax:

```java
do {
    // code
} while (condition);
```

### Example:

```java
int x = 0;
do {
    System.out.println(x);
    x++;
} while (x < 3);
```

✅ Use when **you must do something once before checking**  
Ex: menus, prompts, retries

---

## 🔁 4. `for-each` Loop — _Clean way to loop through collections_

### Syntax:

```java
for (type item : collection) {
    // use item
}
```

### Example:

```java
int[] nums = {1, 2, 3};

for (int n : nums) {
    System.out.println(n);
}
```

✅ Super readable  
❌ No access to index or ability to modify source

---

## ⏹️ Loop Modifiers

### `break`

Immediately exits the loop.

```java
for (int i = 0; i < 10; i++) {
    if (i == 3) break;
    System.out.println(i);
}
```

### `continue`

Skips the current iteration and jumps to next loop.

```java
for (int i = 0; i < 5; i++) {
    if (i == 2) continue;
    System.out.println(i);
}
```

---

## 🔂 Nested Loops

```java
for (int row = 0; row < 3; row++) {
    for (int col = 0; col < 3; col++) {
        System.out.print("[" + row + "," + col + "] ");
    }
    System.out.println();
}
```

⚠️ Complexity grows **exponentially**  
✅ Used in **grids**, **matrix operations**, **games**, etc.

---

## 🧼 Best Practices

- Avoid deep nesting — extract logic to methods
    
- Always guard against **infinite loops**
    
- Use meaningful variable names (`i`, `j`, `index`, `item`)
    
- Use `for-each` for read-only array or list traversal
    
- Use `while` for uncertain termination (e.g. `while (input != "quit")`)
    

---

## 🧪 Real-World Example: Menu with `do...while`

```java
import java.util.Scanner;

public class MenuExample {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int choice;

        do {
            System.out.println("1. Say Hello");
            System.out.println("2. Say Goodbye");
            System.out.println("0. Exit");
            choice = input.nextInt();

            if (choice == 1) {
                System.out.println("Hello!");
            } else if (choice == 2) {
                System.out.println("Goodbye!");
            }

        } while (choice != 0);

        System.out.println("Exited menu.");
    }
}
```

---

## ✅ TL;DR Loop Cheatsheet

```java
// For loop
for (int i = 0; i < n; i++) {...}

// While loop
while (condition) {...}

// Do-while loop
do {...} while (condition);

// For-each loop
for (int x : array) {...}

// Loop modifiers
break;      // exit loop
continue;   // skip to next iteration
```

---
