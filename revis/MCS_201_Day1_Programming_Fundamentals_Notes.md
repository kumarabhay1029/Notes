# 📚 MCS 201 – Day 1 Notes: Programming Fundamentals

---

## 🎯 **Learning Objectives**
- Grasp the problem-solving approach in programming
- Understand algorithms and flowcharts
- Learn the basics of structured programming
- Get introduced to the C language and its features
- Know the structure and compilation process of a C program

---

## 🧩 **1. Problem-Solving Techniques**
### Steps for Problem Solving
1. **Define the Problem** – Clearly understand what is to be solved.
2. **Analyze the Problem** – Identify inputs, outputs, and constraints.
3. **Develop the Solution (Algorithm)** – Write step-by-step instructions.
4. **Test the Solution** – Try the steps with sample data.
5. **Implement in Code** – Translate the solution into a programming language.
6. **Test & Debug** – Run, check outputs, and fix errors.

### Using Computers as Problem-Solving Tools
- Computers execute clear, logical instructions rapidly.
- Programmers must convert real-world problems into logical steps.

---

## 🔗 **2. Basics of Algorithms**
### What is an Algorithm?  
> A finite set of step-by-step, unambiguous instructions to solve a specific problem.

#### ✨ Features of a Good Algorithm
- **Finiteness:** Ends after a finite number of steps.
- **Definiteness:** Each step is clear.
- **Input/Output:** Has defined inputs and outputs.
- **Effectiveness:** Every step is basic and feasible.

#### 📝 Example – Check Prime Number
1. Start
2. Input number N
3. If N < 2, print "Not Prime", Stop
4. For i = 2 to sqrt(N):
    - If N mod i == 0, print "Not Prime", Stop
5. Print "Prime Number"
6. Stop

---

## 🔄 **3. Flowcharts**
- **Definition:** Diagrammatic representation of an algorithm using symbols.
- **Common Symbols:**
  - ⬤ **Oval:** Start/End
  - ▭ **Rectangle:** Process/Instruction
  - ⬨ **Diamond:** Decision/Condition
  - ⧫ **Parallelogram:** Input/Output

#### Example (Prime Check Flowchart Steps)
```
[Start]
   |
[Input N]
   |
[Is N < 2?]--Yes-->[Print "Not Prime"]-->[End]
   |
   No
   |
[Set i = 2]
   |
[Is i ≤ sqrt(N)?]--No-->[Print "Prime"]-->[End]
   |
   Yes
   |
[Is N mod i == 0?]--Yes-->[Print "Not Prime"]-->[End]
   |
   No
   |
[i = i + 1] --> [Back to Is i ≤ sqrt(N)?]
```

---

## 🏗️ **4. Structured Programming Concepts**
- **Sequence:** Execution of statements in order.
- **Selection:** Decision-making using `if`, `else`, `switch`.
- **Iteration:** Repeating actions using loops (`for`, `while`).
- **Top-Down Design:** Break complex problems into manageable modules.
- **Functions:** Each function should perform a single, well-defined task.

---

## 💻 **5. C Language and Its Features**
- **General-purpose, procedural language.**
- **Portable:** Runs on different machines.
- **Efficient:** Produces optimized code.
- **Modular:** Supports functions, structured code.
- **Low-level access:** Can manipulate hardware via pointers.
- **Rich Library:** Many built-in functions.

---

## 🏛️ **6. Structure of a C Program**
```c
#include <stdio.h> // Preprocessor Directive

int main() {       // Main Function
    printf("Hello, World!"); // Output Statement
    return 0;
}
```
- **Sections:**
  - Documentation (comments)
  - Link Section (`#include`)
  - Definition/Global Declarations
  - `main()` Function
  - Subprograms (other functions)

---

## ⚙️ **7. Writing, Compiling & Running C Programs**
- **Write** code using an editor.
- **Save** with `.c` extension.
- **Compile** using compiler (e.g., GCC).
- **Run** the executable.

### **Types of Errors**
- **Syntax:** Typo, missing semicolon, etc.
- **Semantic:** Logic doesn’t match intent.
- **Linker:** Problems with library/function linking.
- **Runtime:** Errors during execution (e.g., divide by zero).
- **Logical:** Output is incorrect due to flawed logic.

---

## 🌟 **Quick Recap**
- Problem-solving in programming is a logical, step-wise approach.
- Algorithms and flowcharts help plan before coding.
- Structured programming leads to better, error-free code.
- C is a foundational language to learn programming basics.

---

> **Next Up:** Data Types, Operators, and Expressions in C!  
> Have a doubt? Ask before proceeding 🚀

---
