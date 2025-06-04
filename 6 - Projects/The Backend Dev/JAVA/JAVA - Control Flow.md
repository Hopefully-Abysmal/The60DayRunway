
---

### 🔀 I. **[[JAVA - Conditionals|Conditionals]]** — _Decision Making_

Let the program **choose a path** based on some logic.

#### `if / else if / else`

```java
int score = 85;

if (score >= 90) {
    System.out.println("Grade: A");
} else if (score >= 80) {
    System.out.println("Grade: B");
} else {
    System.out.println("Needs improvement");
}
```

**Key Notes:**

- Conditions go in `()`
    
- Code blocks go in `{}` — even one-liners (best practice)
    
- `else if` allows chained logic
    
- `else` is the fallback
    

#### `switch` — _Multi-branching for fixed values_

```java
int day = 3;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    default:
        System.out.println("Other day");
}
```

**Use for:** Enums, numbers, chars, Strings, etc.

---

### 🔁 II. **[[JAVA - Loops|Loops]]** — _Repetition Logic_

Let the program **repeat actions** until a condition is met.

#### `for` — _Count-controlled_

```java
for (int i = 0; i < 5; i++) {
    System.out.println("i = " + i);
}
```

|Part|Example|Purpose|
|---|---|---|
|Initialization|`int i=0`|Once before loop|
|Condition|`i < 5`|Before each loop|
|Update|`i++`|After each iteration|

#### `while` — _Condition-controlled_

```java
int count = 0;
while (count < 3) {
    System.out.println("Count: " + count);
    count++;
}
```

- Zero or more executions
    

#### `do...while` — _Guaranteed at least once_

```java
int n = 0;
do {
    System.out.println("n = " + n);
    n++;
} while (n < 3);
```

- Runs the body **before** checking the condition
    

---

### ⏹️ III. **Loop Modifiers**

#### `break` — _Exit loop immediately_

```java
for (int i = 0; i < 10; i++) {
    if (i == 3) break;
    System.out.println(i);
}
```

#### `continue` — _Skip to next loop iteration_

```java
for (int i = 0; i < 5; i++) {
    if (i == 2) continue;
    System.out.println(i);
}
```

---

### 🧠 TL;DR Cheatsheet

```java
// Conditionals
if (x > 0) {...} else {...}
switch (value) { case A: break; ... }

// Loops
for (init; cond; update) {...}
while (cond) {...}
do {...} while (cond);

// Loop Modifiers
break;      // exit loop
continue;   // skip current iteration
```

---
