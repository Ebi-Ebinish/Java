**INSIDE JDK FUNCTIONALITY’S**
**What is JDK?**

**JDK** stands for **Java Development Kit**.

It is a **software development environment** used for developing Java applications. The JDK includes everything needed to **write**, **compile**, **debug**, and **run** Java programs.

1.     Abstract syntax tree
2.     Symbol table
3.     Optimization
4.     Runtime constant pool

**ABSTRACT SYNTAX TREE**

          It used for representation of the source code before compile the file.

An **Abstract Syntax Tree (AST)** is a **tree-like representation of Java source code** used internally by the compiler and tooling APIs to analyze, modify, or compile Java programs.

Java's AST is exposed through the **Java Compiler API**, specifically the `**com.sun.source.tree**` and `**com.sun.source.util**` packages.

 A set of **interfaces** and **tree node types** that represent the structure of a Java program.

 Created by the **Java compiler (javac)** as it parses source code.

**INSIDE JDK FUNCTIONALITIES**

This version will include **in-depth explanations**, **real examples**, and improved formatting.

What is JDK?

**JDK (Java Development Kit)** is a **software development environment** provided by Oracle and other vendors, used for **developing, compiling, debugging, and running Java applications**.

It includes:

·         **JVM (Java Virtual Machine)** – Runs Java bytecode.

·         **JRE (Java Runtime Environment)** – Includes the JVM and runtime libraries.

·         **Compiler (javac)** – Converts Java source code into bytecode (.class files).

·         **Tools** – Debugger (`jdb`), documentation generator (`javadoc`), archiver (`jar`), etc.

 Example:  
When you write a file `Hello.java` and compile it using `javac Hello.java`, the JDK compiles the code into bytecode (`Hello.class`) which the JVM can run.

Internal Functionalities of JDK (with Examples)

### **Abstract Syntax Tree (AST)**

### What is it?

An **Abstract Syntax Tree** is a **hierarchical tree-like structure** that represents the **syntactic structure** of your Java code.

·         Built by the **Java compiler (**`**javac**`**)** during the **parsing phase**.

·         Used for **code analysis, refactoring, static checks**, and **compilation**.

·         Part of the **Java Compiler API** (`com.sun.source.tree`).

Why is it important?

It allows tools (like IDEs, linters, or code analyzers) to **understand the structure** of code in a meaningful way.

Example:

For the code:

public class Hello `{`

```
    
```

```
        System.out.println(
```

```
    }
```

```
}
```

The AST would represent:

·         A class declaration: `Hello`

·         A method: `main`

·         A method call: `System.out.println`

·         A string literal: `"Hello, World!"`

Each of these is a **node** in the tree.

---

### **2. Symbol Table**

###  What is it?

A **Symbol Table** is a data structure used by the compiler to **store information about identifiers** (like variables, classes, methods).

·         Used during **semantic analysis**.

·         Helps the compiler **resolve names** and check **scopes and types**.

Why is it important?

Without a symbol table, the compiler wouldn't know what a variable refers to, whether it has been declared, or whether it's being used correctly.

Example:

For the code:

int x = 10`;`

```
x = x + 
```

The symbol table will store:

| **Identifier** | **Type** | **Scope** |
| -------------- | -------- | --------- |
| x              | int      | Local     |

The compiler uses this table to ensure `x` is declared and used correctly.

---

### **3. Optimization**

###  What is it?

Optimization involves improving the **performance and efficiency** of code—either by the **compiler** or the **JVM** at runtime.

·         **javac (Java compiler)** does minimal optimization.

·         Most optimizations are done by the **JIT (Just-In-Time) compiler** inside the JVM.

Types of Optimization:

·         **Dead code elimination** – Removes code that will never run.

·         **Inlining** – Replaces method calls with the method body to reduce overhead.

·         **Loop unrolling** – Speeds up loops by reducing iterations.

·         **Escape analysis** – Allocates memory on the stack instead of heap when possible.

Example:

Before Optimization:

int x = 5`;`

int y = `x +` 0`;`  // Addition with 0 is useless

After Optimization:

int y = 5`;`  // Simplified

The JVM may apply such simplifications at runtime for performance.

---

### **5.**     **Runtime Constant Pool**

### What is it?

The **Runtime Constant Pool** is a part of the **.class file** that stores:

·         **Literals** – numbers, strings, etc.

·         **Symbolic references** – class names, method names, field names.

It is used by the JVM during execution for:

·         **Dynamic linking** of methods and classes.

·         Efficient reuse of constants.

Example:

For the code:

String msg = "Hello"`;`

The string `"Hello"` is stored **once** in the **constant pool**, and reused if you declare the same string again.

This improves **memory efficiency**.

                             **JIT COMPILER (JUST IN TIME)**

JIT Compiler Optimizations in JVM

The **Just-In-Time (JIT) compiler** is part of the JVM that compiles bytecode to native machine code **at runtime**. This enables dynamic optimizations based on actual program behavior.

### Common JIT Optimizations

·         **Method Inlining:** Replaces method calls with the method body to reduce call overhead.

·         **Dead Code Elimination:** Removes code that will never execute.

·         **Loop Unrolling:** Expands loops to reduce loop overhead and improve instruction-level parallelism.

·         **Constant Folding:** Computes constant expressions at compile or runtime.

·         **Escape Analysis:** Determines if an object can be allocated on the stack instead of the heap, reducing garbage collection.

·         **Adaptive Optimization:** Profiles running code and optimizes “hot” methods that execute frequently.

·         **Register Allocation:** Efficiently assigns variables to CPU registers.

·         **Branch Prediction Optimization:** Reorders code based on likely execution paths.

·         **Inlining Cache:** Speeds up method dispatch by caching resolved methods.

·         **Lock Coarsening and Elimination:** Optimizes synchronization to reduce overhead in multi-threaded code.

·         **Speculative Optimization:** Makes optimistic assumptions about code behavior and can roll back if assumptions fail.

·         **Code Vectorization:** Transforms loops and math operations to use SIMD instructions for parallel processing.

### Why JIT?

·         The JVM can optimize based on **real-time execution data**.

·         Allows Java programs to run nearly as fast as native applications.

·         Provides platform-specific optimizations for different CPUs.