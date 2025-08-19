# MCS-202: Computer System Organization  
## **Day 2: Data Representation Essentials**

---

## **Learning Objectives**
- Convert between number systems.
- Understand character encoding schemes.
- Represent negative numbers using complements.
- Explain fixed and floating point representation, IEEE 754 formats.
- Understand error detection codes.
- Perform computer arithmetic operations.

---

## **1. Number System Conversions**

### Decimal, Binary, Octal, and Hexadecimal

**Conversion Examples:**
- Decimal to Binary: 13 → 1101₂
- Binary to Decimal: 1011₂ → 11₁₀

---

## **2. Character Representation**

### ASCII
- 7-bit encoding, maps characters to numbers (e.g., 'A' = 65)

### Unicode (UTF-8, UTF-16)
- Supports global characters
- UTF-8: Variable-length (1 to 4 bytes)
- UTF-16: Fixed/variable (2 or 4 bytes)

---

## **3. Negative Number Representations**

### 1’s Complement
- Invert all bits (e.g., 5 = 0101; -5 = 1010)

### 2’s Complement
- Invert all bits and add 1 (e.g., 5 = 0101; -5 = 1011)
- Used for binary arithmetic

---

## **4. Fixed Point and Floating Point Representation**

### Fixed Point
- Decimal point at a fixed position
- Suitable for integers and small range decimals

### Floating Point (IEEE 754)

**General Structure:**
```
| Sign (1) | Exponent (8) | Mantissa (23) |  <-- Single precision (32-bit)
```
**Value = (-1)^sign × 1.mantissa × 2^(exponent - bias)**

**Example:**  
24 in binary: 11000₂ = 1.1000 × 2⁴  
Exponent = 4 + 127 = 131  
IEEE Representation:  
- Sign: 0  
- Exponent: 10000011  
- Mantissa: 10000000000000000000000

---

## **5. Normalized Mantissa, Biased Exponent, Precision**

- **Normalized Mantissa:** Always starts with 1 before the decimal (except zero).
- **Biased Exponent:** Stored exponent = actual exponent + bias (127 for single, 1023 for double).
- **Precision:** Single (32 bits), Double (64 bits).

---

## **6. IEEE 754 Format**

### Single Precision (32 bits)
- 1 bit sign, 8 bits exponent, 23 bits mantissa

### Double Precision (64 bits)
- 1 bit sign, 11 bits exponent, 52 bits mantissa

---

## **7. Error Detection Codes**

### Parity Bit
- Adds 1 bit to detect errors (even/odd parity)

### Hamming Code
- Detects and corrects single-bit errors
- Uses extra parity bits for error location

---

## **8. Computer Arithmetic**

### Addition, Subtraction, Multiplication, Division

**Example:**
- 7 + 6 = 1101₂ + 0110₂ = 10011₂ (with overflow check)

---

## **9. Floating Point Arithmetic (Addition, Subtraction, Multiplication, Division)**

**Steps:**
1. Align exponents.
2. Add/subtract mantissas.
3. Normalize result.
4. Handle overflow/underflow.

**Sample Calculation:**
- -7 and 24, their IEEE representation, and stepwise arithmetic (see full example in main chat for details).

---

## **10. Quick Reference Table**

| Concept        | Key Points |
|----------------|-----------|
| Number systems | Binary, Octal, Decimal, Hexadecimal |
| ASCII/Unicode  | Character encoding standards        |
| Complements    | 1’s and 2’s for negative numbers    |
| Floating Point | IEEE 754 Single/Double, normalization, exponent bias |
| Error Codes    | Parity, Hamming                     |
| Arithmetic     | Add, Subtract, Multiply, Divide      |

---

## **Practice Questions**

1. Convert decimal 45 to binary and hexadecimal.
2. Represent -15 in 8-bit 2’s complement.
3. Encode 'A' in ASCII and UTF-8.
4. Add 1.5 and 2.25 in IEEE 754 floating point format.

---

**End of Day 2 Notes**