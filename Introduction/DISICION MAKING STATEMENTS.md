## Tricky in switch case:

### Allowed types (across versions)

**Primitive integral types:**
- byte  
- short  
- char  
- int  

**Wrapper equivalents (auto-unboxing works):**
- Byte  
- Short  
- Character  
- Integer  

- enum types (since Java 5)  
- String (since Java 7)  
### Not allowed (even in Java 21+ as of today)

- long  
- float  
- double  
- boolean  

---
## Break Statement

The break statement is used to terminate the innermost enclosing loop (for, while, do-while) or a switch statement immediately, and control jumps to the statement after the loop/ switch.
### Labelled break

In nested loops, a normal break only exits the inner loop.  
But with labels, you can exit outer loops directly.

### Syntax

Labele_Name:

The label is: `outer:`
### Code Ex:

```java
outer: // label for outer loop
for (int i = 0; i < 3; i++) {
    for (int j = 0; j < 3; j++) {
        if (i == 1 && j == 1)
            break outer;   // terminates BOTH loops
        System.out.println(i + " " + j);
    }
}
System.out.println("Exited all loops");
```

## Continue Statement:

The continue statement is used to skip the current iteration of a loop and directly jump to the next iteration. It does not terminate the loop, only skips the remaining part of the current iteration.
### Code Ex:

```java
for (int i = 0; i < 5; i++) {     if (i == 2)         continue; // skip when i=2     System.out.println(i); }
```

---
## Labeled continue

With nested loops, a normal continue only skips the current inner loop iteration.  
But a labeled continue can skip the outer loop iteration completely.

```java
outer: // label for outer loop for (int i = 0; i < 3; i++) {     for (int j = 0; j < 3; j++) {         if (j == 1)             continue outer; // skips outer loop iteration when j==1         System.out.println(i + " " + j);     } }
```

---
## Key Difference: break vs return

|Keyword|Effect|
|---|---|
|break|Exits only the nearest loop, execution continues after the loop.|
|return|Exits the entire method, execution control goes back to the caller.|

---
## How this works:

1. `int i = 1` → initialization (runs once)
2. `i <= 5` → condition is checked
3. If true, the loop body executes: `System.out.println(...)`
4. Then, `i++` → update step
5. Go back to step 2

---
## What is Maximal munch principle?

When reading the source code, the compiler should always consume the longest sequence of characters that can form a valid token.

### The Token are:

- **Identifiers:** variable name, ClassName.
- **Keywords:** if, for, while, class, int.
- **Operators:** +, -, ++, --, *.
- **Literals:** 10(Integer), “Hello”(String), ‘A’(char).
- **Separators:** ; , , , (, ).
### Ex:

`i+++i`
