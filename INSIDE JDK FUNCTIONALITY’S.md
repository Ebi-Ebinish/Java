
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

