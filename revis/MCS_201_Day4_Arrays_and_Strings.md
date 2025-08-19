# 🧮 MCS_201 – Day 4 Notes: Arrays & Strings in C

---

## 🎯 **Learning Objectives**
- Understand array declaration, initialization, and processing (1D & 2D)
- Use character arrays (strings) and their initialization
- Work with array subscripts and multi-dimensional arrays
- Learn string declaration, display, arrays of strings, and standard string functions

---

## 1️⃣ **Arrays in C**

### 📦 **What is an Array?**
An **array** is a collection of elements of the same data type, stored in contiguous memory locations and accessed by index.

- **1D Array:** Linear collection (like a row of boxes)
- **2D Array:** Table/matrix (rows and columns)

---

### 📝 **Array Declaration**

**Syntax:**
```c
data_type array_name[size];
```
**Examples:**
```c
int marks[5];
float temperature[7];
char vowels[5];
```

---

### ✍️ **Array Initialization**

**At Declaration:**
```c
int numbers[4] = {10, 20, 30, 40};
```
- If fewer elements are given, remaining are set to zero:
```c
int arr[5] = {1, 2}; // arr = 1, 2, 0, 0, 0
```

**After Declaration:**
```c
numbers[0] = 5;
numbers[1] = 10;
```

---

### 🔢 **Accessing Array Elements (Subscripts)**
- Indexing starts at 0.
- `marks[0]` is the first element, `marks[4]` is the fifth.

**Example:**
```c
for(int i = 0; i < 5; i++) {
    printf("%d ", marks[i]);
}
```

---

## 2️⃣ **Multi-Dimensional Arrays**

### 🧊 **2D Array Declaration & Initialization**

**Syntax:**
```c
data_type array_name[rows][columns];
```
**Example:**
```c
int matrix[2][3] = { {1, 2, 3}, {4, 5, 6} };
```

**Accessing Elements:**
- `matrix[0][1]` is the value in first row, second column (value: 2)

---

### 🖨️ **Processing 2D Arrays (Nested Loops Example)**
```c
for(int i = 0; i < 2; i++) {
    for(int j = 0; j < 3; j++) {
        printf("%d ", matrix[i][j]);
    }
    printf("\n");
}
```
**Output:**
```
1 2 3 
4 5 6 
```

---

## 3️⃣ **Strings in C (Character Arrays)**

### ✨ **Declaration and Initialization**

**Manual (with '\0'):**
```c
char name[6] = {'A', 'l', 'i', 'c', 'e', '\0'};
```

**String Literal:**
```c
char city[] = "Delhi"; // Auto null-terminated
```

---

### 📢 **Displaying Strings**

- Use `%s` in `printf`:
```c
printf("%s", city);
```

---

### 📚 **Array of Strings**
- Useful for storing multiple words/names.

**Example:**
```c
char names[3][10] = { "Ram", "Shyam", "Geeta" };
for(int i = 0; i < 3; i++) {
    printf("%s\n", names[i]);
}
```

---

### 🛠️ **Standard String Functions (`<string.h>`)**

| Function         | Purpose                | Example Usage                      |
|------------------|-----------------------|------------------------------------|
| `strlen(str)`    | Length of string      | `int len = strlen(name);`          |
| `strcpy(dest, src)` | Copy string        | `strcpy(dest, src);`               |
| `strcat(dest, src)` | Concatenate        | `strcat(s1, s2);`                  |
| `strcmp(s1, s2)`   | Compare strings     | `if(strcmp(a, b) == 0)`            |

**Example:**
```c
#include <string.h>
char s1[20] = "Hello";
char s2[] = "World";
strcat(s1, s2); // s1 becomes "HelloWorld"
```

---

## 4️⃣ **Array Processing Examples**

### 🔢 **Sum of Array Elements**
```c
int arr[5] = {1, 2, 3, 4, 5}, sum = 0;
for(int i = 0; i < 5; i++) {
    sum += arr[i];
}
printf("Sum = %d", sum); // Output: 15
```

---

### 🖨️ **Reading and Printing a 2D Array**
```c
int a[2][2];
printf("Enter 4 numbers:\n");
for(int i = 0; i < 2; i++) {
    for(int j = 0; j < 2; j++) {
        scanf("%d", &a[i][j]);
    }
}
printf("You entered:\n");
for(int i = 0; i < 2; i++) {
    for(int j = 0; j < 2; j++) {
        printf("%d ", a[i][j]);
    }
    printf("\n");
}
```

---

### 🔤 **Input and Display a String**
```c
char str[20];
printf("Enter your name: ");
scanf("%s", str); // For single word input
printf("Hello, %s!", str);
```
*Use `fgets(str, 20, stdin);` for multi-word.*

---

## ⭐ **Quick Recap Table**

| Concept        | Purpose/Use Case                   | Syntax/Example                |
|----------------|------------------------------------|-------------------------------|
| 1D Array       | List of items                      | `int a[5];`                   |
| 2D Array       | Table or matrix                    | `int m[3][3];`                |
| String         | Series of characters with `\0`     | `char s[] = "ABC";`           |
| Array of String| List of words/names                | `char n[3][10] = {...};`      |
| String Fn      | Manipulate/display string data     | `strlen, strcpy, strcat, ...` |

---

## 🧑‍🎓 **Practice Exercises**

1. **Declare and initialize a 2D array for a 3x2 matrix and print it.**
2. **Write a C program to input 5 numbers in an array and print their sum and average.**
3. **Write a program to input a string and print its length using `strlen`.**
4. **Store 3 names in an array of strings and print each on a new line.**

---

## 💡 **Tips & Common Mistakes**
- Array indices start at 0!
- Strings in C must end with `'\0'` (null character).
- Always include `<string.h>` for string functions.
- Be careful with array bounds to avoid memory errors.
- For multi-word string input, use `fgets()` instead of `scanf("%s", ...)`.

---

> **Next Up:** Functions in C!  
> Have questions? Ask before we proceed 🚀

---
