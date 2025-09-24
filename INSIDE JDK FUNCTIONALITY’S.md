
# What is JDK?

**JDK** stands for **Java Development Kit**.

It is a **software development environment** used for developing Java applications. The JDK includes everything needed to **write**, **compile**, **debug**, and **run** Java programs.

### Key Components:

1. Abstract Syntax Tree  
2. Symbol Table  
3. Optimization  
4. Runtime Constant Pool  

---

## Abstract Syntax Tree (AST)

### What is it?

It is used to represent the source code **before compilation**.

An **Abstract Syntax Tree (AST)** is a **tree-like representation** of Java source code used internally by the compiler and tooling APIs to analyze, modify, or compile Java programs.

- Java's AST is exposed through the **Java Compiler API**:
  - `com.sun.source.tree`
  - `com.sun.source.util`
- A set of **interfaces and tree node types** that represent the structure of a Java program.
- Created by the **Java compiler (`javac`)** during parsing.

### Why is it important?

It allows tools (like IDEs, linters, or analyzers) to **understand and manipulate code structure** meaningfully.

### Example:

Java Code:
```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

The AST would represent:

- A class declaration: `Hello`
- A method: `main`
- A method call: `System.out.println`
- A string literal: `"Hello, World!"`

Each of these is a **node** in the tree.

---

## 2. Symbol Table

### What is it?

A **Symbol Table** is a data structure used by the compiler to store information about identifiers (like variables, classes, methods).

- Used during **semantic analysis**.
- Helps the compiler **resolve names** and check **scopes and types**.

### Why is it important?

Without a symbol table, the compiler wouldn't know what a variable refers to, whether it has been declared, or whether it's being used correctly.

### Example:

For the code:

```java
int x = 10;
x = x + 5;

```

The symbol table will store:

| Identifier | Type | Scope |
|------------|------|-------|
| x          | int  | Local |

The compiler uses this table to ensure `x` is declared and used correctly.

---

## 3. Optimization

### What is it?

Optimization involves improving the performance and efficiency of code—either by the compiler or the JVM at runtime.

- `javac` (Java compiler) does minimal optimization.
- Most optimizations are done by the **JIT (Just-In-Time) compiler** inside the JVM.

### Types of Optimization:

- **Dead code elimination** – Removes code that will never run.
- **Inlining** – Replaces method calls with the method body to reduce overhead.
- **Loop unrolling** – Speeds up loops by reducing iterations.
- **Escape analysis** – Allocates memory on the stack instead of heap when possible.

### Example:

Before Optimization:

```java
int x = 5;
int y = x + 0;  // Addition with 0 is useless

```

After Optimization:

```java
int y = 5;  // Simplified
```



