# OPERATORS

## What is truncated?

Truncation means removing the fractional (decimal) part of a number — usually when converting from a floating-point number (float, double) to an integer (int, long).

Int num1=10;  
Int num2=20;  

If both operands are integers, the result will be an integer – any decimal part is truncated,  

If you want to get the exact result, make any variable type to floating point (float, double) data types.

Int num1=10;  
Float num2=20;  

You can make change when declaration or you can use type casting also.  

Ex:  
System.out.println((float)num1 / num2);

---

# TYPE PROMOTION

## 1. Integer Arithmetic Promotions

| Operand 1 | Operand 2 | Promoted To | Why |
|------------|------------|------------|-----|
| byte | byte | int | All byte/short/char are promoted to int before operation |
| short | short | int | Same reason |
| char | char | int | Same |
| byte | short | int | Mixed → promote both to int |
| char | int | int | Promote char to int |
| byte | int | int | Promote byte to int |

---

## 2. Mixed-Type Arithmetic Promotions

When two different types are used, Java promotes to the widest type involved:

| Operand 1 | Operand 2 | Result Type |
|------------|------------|------------|
| int | long | long |
| int | float | float |
| long | float | float |
| int | double | double |
| float | double | double |
| long | double | double |

---

# Unary Operator

| Expression | First Happens | Then Happens | Final x | Value Stored in Variable (y) |
|------------|---------------|--------------|----------|-------------------------------|
| ++x | x = x + 1 → 11 | Use x | 11 | 11 |
| x++ | Use x → 10 | x = x + 1 → 11 | 11 | 10 |
| --x | x = x - 1 → 9 | Use x | 9 | 9 |
| x-- | Use x → 10 | x = x - 1 → 9 | 9 | 10 |

---

# Bitwise Not Operator (~)

~ is the bitwise NOT operator — it flips every bit in the binary representation of a number.

Turns 1 into 0  
Turns 0 into 1  

---

# Short circuiting in Operator

&&, || → skip unnecessary checks → safer, faster.

---

# Ternary Operator

The ternary operator (?:) is a conditional operator in Java that evaluates a boolean condition and chooses one of two values.  

The syntax:  
result = (condition) ? value_if_true : value_if_false;  

It’s basically a shortcut for if-else but as an expression (returns a value).

---

# Bitwise Operator

Bitwise operators work at the bit level (binary representation of numbers).  

They treat numbers as sequences of 0s and 1s, not as decimal values.

---

## 1. Bitwise & AND

Compares each bit of two numbers. Result is 1 if both bits are 1, else 0.

Ex:  
```java
int a = 5;   // 0101 (binary)
int b = 3;   // 0011 (binary)
System.out.println(a & b); // 0001 = 1.
```

---
## 2. | Bitwise OR

Compares each bit of two numbers. Result is 1 if any bit is 1.

Ex:
```java
int a = 5;   // 0101
int b = 3;   // 0011
System.out.println(a | b); // 0111 = 7

```

