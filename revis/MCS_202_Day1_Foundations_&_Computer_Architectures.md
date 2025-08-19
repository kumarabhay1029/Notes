# MCS-202: Computer System Organization  
## **Day 1: Foundations & Computer Architectures**

---

## **Learning Objectives**
- Understand the basic components and architectures of computer systems.
- Explain Von Neumann, CISC, RISC, Mobile, and Multiprocessor Architectures.
- Describe instruction execution with a simple register set.

---

## **1. Different Architectures of Computer Systems**

### 1.1 What is Computer Architecture?
Computer architecture refers to the design, structure, and functioning of a computer’s components and their interrelations.

---

### 1.2 Von Neumann Architecture

**Definition:**  
A computer architecture model where a single memory is used for both data and instructions.

**Diagram:**
```
+---------------------+
|     Input Device    |
+----------+----------+
           |
           v
+---------------------+
|    Control Unit     |
+----------+----------+
           |
           v
+---------------------+
|     ALU/Processor   |
+----------+----------+
           |
           v
+---------------------+
|        Memory       |
+----------+----------+
           |
           v
+---------------------+
|     Output Device   |
+---------------------+
```

**Key Features:**
- Single memory for data and program
- Sequential instruction execution (FETCH, DECODE, EXECUTE)
- Simpler design, but bottleneck due to shared memory bus ("Von Neumann bottleneck")

---

### 1.3 CISC vs. RISC Architectures

#### CISC (Complex Instruction Set Computer)
- Large, complex instruction set (multi-cycle instructions)
- Emphasizes hardware for complex tasks
- Example: x86 processors

#### RISC (Reduced Instruction Set Computer)
- Small, simple set of instructions (mostly single-cycle)
- Emphasizes software for complex tasks
- Example: ARM, MIPS processors

**Comparison Table:**

| Feature         | CISC                  | RISC                   |
|-----------------|----------------------|------------------------|
| Instruction Set | Complex, many         | Simple, few            |
| Execution Time  | Multi-cycle           | Single-cycle           |
| Code Size       | Small                 | Large                  |
| Hardware        | Complex               | Simple                 |

---

### 1.4 Mobile Architecture

- Designed for low power, high efficiency (e.g., ARM Cortex series)
- Optimized for portable devices (smartphones, tablets)
- Features: energy efficiency, system-on-chip (SoC) integration, specialized hardware for multimedia

---

### 1.5 Multiprocessor Architectures

- Systems with two or more CPUs working in parallel
- Used for improved performance, reliability
- Types: Symmetric Multiprocessing (SMP), Asymmetric Multiprocessing (AMP)

**Diagram:**
```
+---------+    +---------+    +---------+
|  CPU 1  |    |  CPU 2  |    |  CPU N  |
+----+----+    +----+----+    +----+----+
     |              |              |
     +--------------+--------------+
                    |
                +---+---+
                | Memory|
                +-------+
```

---

## **2. Instruction Set Architecture (ISA)**

- Defines the set of instructions a processor can execute
- Determines how software communicates with hardware

---

## **3. Instruction Execution Using Simple Register Set**

### Steps in Instruction Cycle:
1. **Fetch:** Get instruction from memory
2. **Decode:** Interpret the instruction
3. **Execute:** Perform the operation
4. **Store:** Write result back (if needed)

**Basic Registers:**
- **Program Counter (PC):** Address of next instruction
- **Instruction Register (IR):** Holds current instruction
- **Accumulator (ACC):** Temporary storage for calculations

---

**Summary Diagram: Instruction Execution**
```
[PC] --> [Memory] --> [IR] --> [Control Unit/ALU] --> [ACC]
```

---

## **Key Terms**
- **Architecture:** Design of a computer system
- **Von Neumann Bottleneck:** Performance limitation due to shared memory bus
- **CISC/RISC:** Instruction set philosophies
- **Multiprocessor:** Multiple CPUs for parallelism

---

## **Quick Review Questions**
1. What is the main difference between Von Neumann and Harvard architecture?
2. Give one advantage and one disadvantage of multiprocessor systems.
3. What is an instruction set?

---

**End of Day 1 Notes**