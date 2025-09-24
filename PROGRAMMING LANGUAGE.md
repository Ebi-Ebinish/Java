# Programming Concepts Notes

## What is a Programming Language?

It is a bridge between the user and the computer to communicate. Computers understand only binary (0s and 1s).

---

## What is a Low-Level Language?

- Reaches hardware quickly via a short path.
- Communicates directly with the CPU.
- Response is very fast.

**Example:** Assembly Language

### Extra Knowledge:
- Assembly language is a **low-level programming language** that is closely related to a computer’s machine code (binary instructions).
- It is very complex for humans to understand.

**What it is:**
- Assembly provides human-readable instructions that correspond directly to the CPU’s machine instructions.
- Used to build OS, hardware drivers, etc.

---

## What is a High-Level Language?

- Reaches hardware with some intermediate steps, not directly.
- Requires translation using a **compiler** or **interpreter**.
- Response time is slower than low-level languages.

**Examples:** Java, C++, Python

---

## What is Compilation?

- Compilation transforms source code into executable code.
- It happens **before** the program is run.

---

## What is an Interpreter?

- An interpreter is a tool.
- It **executes code line by line**, converting it into machine-understandable code on the fly.
- Slower than compiled code but easier for testing and debugging.

---

## What is Platform Independence?

### First, understand what a **Platform** is:
- **Hardware:** (CPU architecture, instruction set) e.g., Intel x86, ARM, RISC-V
- **Operating System (OS):** e.g., Windows, Linux, macOS

### Platform Dependency:
- If you compile a C program on Windows, it won’t run on Linux unless recompiled.

### Platform Independence:
- Java achieves platform independence.
- Once compiled into bytecode (`.class` or `.jar`), the code can run on any OS or hardware **with a JVM**.

### Compilation into Bytecode:
- The Java compiler (`javac`) compiles `.java` files into **bytecode** (`.class` files).
- Bytecode is **not machine code**, but an **intermediate representation** understood by the **Java Virtual Machine (JVM)**.

### JVM Execution:
- Each platform has its own JVM implementation.
- JVM either **interprets** or **JIT-compiles** the bytecode into native machine code for that system.

**Example:**
- On Windows → JVM converts bytecode to Windows x86 instructions.
- On Linux ARM → JVM converts bytecode to ARM instructions.

**Result:** One compiled `.class` file can run anywhere!

---

## What is a Functional Language?

- A functional language consists of instructions forming an algorithm.
- Focuses on **what to solve**, not **how to solve** it.

---

## Imperative vs Declarative

- **Imperative Programming:** Focuses on *how* to achieve a task (step-by-step).
- **Declarative Programming:** Focuses on *what* the program should accomplish.

---

## Functional Language vs Procedural Language

- **Functional:** Emphasizes immutability, pure functions.
- **Procedural:** Based on a sequence of steps or procedures.

---

## OOPs (Object-Oriented Programming)

> *Note: You can expand this section based on your specific learning topics (e.g., classes, objects, inheritance, polymorphism).*

---

## What is Memory Management?

- When a program runs, a **process** is created.
- Each process has a **main thread** where the main function is triggered.
- Each process is **isolated** from others.
- A **virtual address space** is created per process, mapping to physical memory (RAM).

### Virtual Address Space Segments:

- **Code Segment**: Contains executable instructions (read-only).
- **Data Segment**: Stores global and static variables.
- **BSS (Block Started by Symbol)**: Stores uninitialized/static variables.
- **Heap**: Used for dynamic memory allocation (Java objects are stored here).
- **Stack**: LIFO structure for function calls, local variables, return types.
- **Registers**: Used for temporary CPU operations.

---

## Summary of Memory Segments:

| Segment      | Description                                        |
|--------------|----------------------------------------------------|
| Code         | Machine instructions; read-only                    |
| Data Segment | Initialized global/static variables                |
| BSS          | Uninitialized/static variables                     |
| Heap         | Dynamic memory; used for objects (Java heap)       |
| Stack        | Function calls, arguments, local variables         |
| Registers    | Temporary fast-access storage for CPU instructions |
