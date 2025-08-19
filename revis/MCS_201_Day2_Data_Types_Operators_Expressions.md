# 📘 MCS 201 – Day 2 Notes: Data Types, Operators & Expressions in C

---

## 🎯 **Learning Objectives**
- Understand the C character set, identifiers, and keywords
- Declare and use variables, constants, and data types
- Use preprocessor directives, assignment statements, and operators
- Understand operator precedence and associativity

---

## 1️⃣ **Character Set in C**

The **character set** defines all the valid characters that can be used in a C program.

- **Letters:** A–Z, a–z  
- **Digits:** 0–9  
- **Special Symbols:** `+ - * / = % & # @ $ _ ; : " ' < > ( ) { } [ ] , . ? ! ^ | \`  
- **White Spaces:** space, tab, newline

**Example:**
```c
int sum_1 = a + b;
```
All characters used here are valid in C.

---

## 2️⃣ **Identifiers and Keywords**

### **Identifiers**
Identifiers are names given to variables, functions, arrays, etc.

**Rules for forming identifiers:**
- Must start with a letter or underscore (`_`)
- Can contain letters, digits, and underscores
- Cannot use spaces or special characters (except `_`)
- Case-sensitive (`Total` and `total` are different)
- Cannot be a keyword

**Examples:**  
`marks`, `student1`, `_main`, `sum_2024`, `totalCount`

### **Keywords**
Keywords are reserved words that have special meaning in C.

**Common keywords:**  
`int`, `float`, `if`, `else`, `for`, `while`, `return`, `break`, `char`, `void`, `double`, `switch`, `case`, `const`, `struct`, `enum`, `typedef`, `sizeof`, `goto`, `continue`, `static`, `unsigned`, `signed`, `long`, `short`

*Keywords cannot be used as identifiers.*

---

## 3️⃣ **Data Types and Storage**

### **Primary Data Types:**

| Data Type | Description                  | Example        |
|-----------|------------------------------|----------------|
| int       | Integer (whole numbers)      | 10, -5, 0      |
| float     | Floating point (decimals)    | 3.14, -2.7     |
| char      | Single character             | 'A', 'z', '4'  |
| double    | Double-precision decimal     | 2.789456       |

#### **Qualifiers:**  
- `long`, `short`, `signed`, `unsigned`
- Example: `unsigned int x;`, `long int y;`

### **Variables**
Variables are named locations in memory used to store data.

**Declaration:**  
```c
int age;
float percentage;
```

**Initialization:**  
```c
int age = 19;
char grade = 'A';
```

### **Constants**
A constant is a value that does not change during the execution of a program.

#### Types of Constants:
- **Integer constants:** `1`, `-10`, `456`
- **Floating point constants:** `3.14`, `-0.001`
- **Character constants:** `'A'`, `'z'`, `'9'`
- **String constants:** `"Hello"`, `"C Programming"`

#### **Symbolic Constants:**  
Defined using `#define`
```c
#define PI 3.14159
#define MAX 100
```
*Symbolic constants make code easier to maintain.*

---

## 4️⃣ **Preprocessor Directives**

Preprocessor directives are commands that are executed before the actual compilation of code begins.  
They always start with a `#`.

**Examples:**
- `#include <stdio.h>` – includes the standard input/output library
- `#define PI 3.14159` – defines a symbolic constant

---

## 5️⃣ **Assignment Statements**

Assignment statements are used to assign values to variables.

**Syntax:**  
`variable = value;`

**Example:**  
```c
sum = a + b;
marks = 95;
```

---

## 6️⃣ **Operators in C**

### **Arithmetic Operators**
| Operator | Description    | Example (`a=5`, `b=2`) | Result |
|----------|---------------|------------------------|--------|
| +        | Addition      | a + b                  | 7      |
| -        | Subtraction   | a - b                  | 3      |
| *        | Multiplication| a * b                  | 10     |
| /        | Division      | a / b                  | 2      |
| %        | Modulus       | a % b                  | 1      |

### **Relational Operators**
| Operator | Description        | Example | Result |
|----------|-------------------|---------|--------|
| ==       | Equal to          | a == b  | 0      |
| !=       | Not equal to      | a != b  | 1      |
| >        | Greater than      | a > b   | 1      |
| <        | Less than         | a < b   | 0      |
| >=       | Greater or equal  | a >= b  | 1      |
| <=       | Less or equal     | a <= b  | 0      |

### **Logical Operators**
| Operator | Description        | Example        | Result |
|----------|-------------------|----------------|--------|
| &&       | Logical AND       | (a > 0 && b > 0) | 1    |
| \|\|     | Logical OR        | (a > 0 \|\| b < 0) | 1  |
| !        | Logical NOT       | !(a > 0)       | 0      |

### **Other Operators**
- **Assignment:** `=`
- **Comma:** `,`
- **Conditional (Ternary):** `? :`  
  Example: `result = (a > b) ? a : b;`
- **Type cast:** `(type)`  
  Example: `float x = (float) a / b;`
- **sizeof:** `sizeof(variable)`  
  Example: `int size = sizeof(int);`
- **Shorthand operators:** `+=`, `-=`, `*=`, `/=`, etc.  
  Example: `a += 5;` (*equivalent to* `a = a + 5;`)

---

## 7️⃣ **Operator Precedence and Associativity**

When an expression contains multiple operators, **operator precedence** determines which operator is evaluated first.

**Example:**
```c
int result = 2 + 3 * 4; // result = 2 + (3*4) = 14
```
- `*` has higher precedence than `+`, so multiplication happens before addition.

**Associativity:**  
When two operators of the same precedence appear, associativity determines the order of evaluation (usually left to right).

---

## 8️⃣ **Examples**

### Example 1: Variable Declaration, Initialization and Assignment
```c
#include <stdio.h>
#define PI 3.14159

int main() {
    int radius = 5;
    float area;
    area = PI * radius * radius;
    printf("Area = %f\n", area);
    return 0;
}
```

### Example 2: Using Different Operators
```c
#include <stdio.h>

int main() {
    int a = 10, b = 3;
    printf("a + b = %d\n", a + b);
    printf("a - b = %d\n", a - b);
    printf("a * b = %d\n", a * b);
    printf("a / b = %d\n", a / b);
    printf("a %% b = %d\n", a % b);
    printf("a > b = %d\n", a > b);
    printf("a == b = %d\n", a == b);
    return 0;
}
```
*Note: `%%` is used in `printf` to print a `%` sign.*

---

## 9️⃣ **Quick Recap**

- C uses a rich character set for writing programs.
- Identifiers must follow certain rules; keywords are reserved.
- Data types specify what kind of data a variable can hold.
- Preprocessor directives are handled before compilation.
- Operators perform various computations and comparisons.
- Operator precedence and associativity affect how expressions are evaluated.

---

## 🌟 **Practice Questions**
1. What is the difference between a keyword and an identifier?
2. Declare and initialize a float variable in C.
3. What will be the output of `printf("%d", 9/2);`?
4. Is `sum&total` a valid identifier? Why or why not?
5. Write a symbolic constant for the value of gravity as `9.8` in C.

---

> **Next Up:** Decision and Loop Control Statements in C (if, switch, loops, etc.)  
> Have a doubt? Ask before proceeding! 🚀

---
