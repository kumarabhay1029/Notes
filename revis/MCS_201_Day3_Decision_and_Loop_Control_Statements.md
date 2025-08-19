# 🚦 MCS 201 – Day 3 Notes: Decision & Loop Control Statements in C

---

## 🎯 **Learning Objectives**
- Master decision-making using `if`, `if-else`, and `switch`
- Use loops: `while`, `do-while`, `for`, and nested loops
- Understand and apply special statements: `goto`, `break`, and `continue`
- Write error-free, logical, and efficient C code

---

## 1️⃣ **Decision Control Statements**

### 🔹 The `if` Statement

Allows you to make choices in your program based on conditions.

```c
if (condition) {
    // Code to execute if condition is true
}
```

#### Example:
```c
int age = 20;
if (age >= 18) {
    printf("You are eligible to vote.\n");
}
```

---

### 🔹 The `if-else` Statement

Executes one block if the condition is true, another if false.

```c
if (marks >= 40) {
    printf("Pass\n");
} else {
    printf("Fail\n");
}
```

---

### 🔹 The `else-if` Ladder

For multiple conditions.

```c
if (score >= 90)
    printf("Grade: A\n");
else if (score >= 75)
    printf("Grade: B\n");
else if (score >= 60)
    printf("Grade: C\n");
else
    printf("Grade: D\n");
```

---

### 🔹 The `switch` Statement

Efficient for handling multiple fixed choices.

```c
switch (expression) {
    case value1:
        // code
        break;
    case value2:
        // code
        break;
    ...
    default:
        // code
}
```

#### Example:
```c
int day = 2;
switch(day) {
    case 1: printf("Monday\n"); break;
    case 2: printf("Tuesday\n"); break;
    case 3: printf("Wednesday\n"); break;
    default: printf("Other day\n");
}
```
- `break` prevents fall-through.
- `default` runs if no case matches.

---

## 2️⃣ **Loop Control Statements**

Loops repeat a block of code.

### 🔹 The `while` Loop

Checks the condition before each iteration.

```c
int i = 1;
while (i <= 5) {
    printf("%d ", i);
    i++;
}
```
*Output: 1 2 3 4 5*

---

### 🔹 The `do-while` Loop

Executes at least once, checks condition after each iteration.

```c
int i = 1;
do {
    printf("%d ", i);
    i++;
} while (i <= 5);
```
*Output: 1 2 3 4 5*

---

### 🔹 The `for` Loop

Best when number of iterations is known.

```c
for (int i = 1; i <= 5; i++) {
    printf("%d ", i);
}
```
*Output: 1 2 3 4 5*

---

### 🔹 Nested Loops

A loop inside another loop. Useful for tables, patterns, matrices.

```c
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 2; j++) {
        printf("i=%d, j=%d\n", i, j);
    }
}
```

---

## 3️⃣ **Special Statements**

### 🔹 The `goto` Statement

Jumps to a labeled statement. **Avoid unless necessary**.

```c
goto label;
// ... other code
label:
    printf("Jumped here!\n");
```

---

### 🔹 The `break` Statement

Exits from loops or switch immediately.

```c
for (int i = 1; i <= 10; i++) {
    if (i == 5) break;
    printf("%d ", i); // prints 1 2 3 4
}
```

---

### 🔹 The `continue` Statement

Skips to the next loop iteration.

```c
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue;
    printf("%d ", i); // prints 1 2 4 5
}
```

---

## ⭐ **Quick Recap Table**

| Statement   | Used For                        | Example Use                |
|-------------|---------------------------------|----------------------------|
| `if`        | Single condition check          | Eligibility, pass/fail     |
| `if-else`   | Two-way decision                | Even/odd, pass/fail        |
| `else-if`   | Multiple conditions             | Grading, menu options      |
| `switch`    | Multi-way branching             | Days, menu selections      |
| `while`     | Unknown repetitions             | Input until valid          |
| `do-while`  | At least one execution          | Menu loops, retry logic    |
| `for`       | Known number of repetitions     | Counting, arrays, tables   |
| `break`     | Exit loop or switch immediately | Early stop on condition    |
| `continue`  | Skip current iteration          | Skip invalid data          |

---

## 📝 **Practice Exercise**

1. **Write a program to print all even numbers from 1 to 20 using a for loop and continue statement.**
2. **Create a menu-driven program using switch to perform +, -, *, / on two numbers.**
3. **Explain with an example: What happens if you forget `break` in a switch case?**

---

## 🎓 **Tips & Best Practices**
- Prefer structured loops (`for`, `while`) over `goto`.
- Always use `break` in switch cases to prevent fall-through errors.
- Use `continue` to skip unnecessary processing inside loops.
- Design your logic before coding to avoid infinite loops or missed cases.

---

> **Next Up:** Arrays & Strings in C  
> Got doubts? Ask before we proceed! 🚀

---