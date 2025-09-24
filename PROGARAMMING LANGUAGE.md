	**What is programming language?**

          It is a bridge a between user and computer to communicate. Computer understand language is 0’s and 1’s, binary format.

**What is low level language?**

          It reaches the Hardware quickly with a short way. It communicates directly to the CPU. The response will be very quick.

          Example: Assembly language

**Extra KN:**

Assembly language is a **low-level programming language** that is closely related to a computer’s machine code (binary instructions).

It very high complex to understand by a human.

**What it is:**

Assembly language provides human-readable instructions that correspond directly to the CPU’s machine instructions.

Use to build like OS, Hardware drivers, etc.

**What is High level language?**

          It reaches the Hardware with some step with a little bit long way compare to low level language. It not communicates directly to the CPU. The response will may take some time.

          In between the software to hardware we have one steps like intermediator (Compiler).

          Ex: Java, C++, Python

**What is compilation?**

          When you compile you source code. It completely taking changing your source code to executable code.

**What is Interpreter?**

          Interpreter it a tool. It executes line by line for machine understandable code to a hardware and the hardware taking that code and giving the result for that code.

### **What is platform independent?**

          First understand platform,

**Hardware (CPU architecture, instruction set)** → e.g., Intel x86, ARM, RISC-V

**Operating System (OS)** → e.g., Windows, Linux, macOS.

**Platform dependency means**

If you compile a C program on Windows, it won’t run on Linux unless you recompile it. This is **platform dependency**.

**Platform Independent:**

Once you compile Java code, the **same compiled file** (`.class` / `.jar`) can run on **any OS and any hardware**, provided a **Java Virtual Machine (JVM)** exists for that platform.

**Compilation into Bytecode (`.class`)**

The **Java Compiler (**`**javac**`**)** compiles `.java` files into **bytecode**. Bytecode **not machine code**.

It’s an **intermediate representation**: set of instructions understood by the **JVM**.

**JVM Executes Bytecode**

Every platform (Windows, Linux, macOS, Android, etc.) has its **own implementation of JVM**.

The JVM **interprets or JIT-compiles** the bytecode into the **native machine code** of that system.

Example: On Windows, JVM converts bytecode → Windows x86 instructions. On Linux ARM, JVM converts bytecode → ARM instructions.

This means **one compiled** `**.class**` **file can run anywhere**.

**What is Functional Language?**

          Set of instruction for an algorithm.

What is imperative and what is declarative.

Functional language and procedural Language.

OPPS

**What is Memory management?**

          When you create a program it always create a processer. Inside a processer there will be created a thread that is called main thread using that main thread we are triggering our main function.

          Each processer is isolated between one to another.

          When the processer is created there will be automatically created virtual address space (Memory).

That virtual address space has individual data segment,

The virtual address space connect the physical address space like RAM.

Code part    --à This and all will be inside a processer

Data segment

BSS

Heap

Stack  à Each stack has individual thread

Register

This and all basically connect to the physical Address that means Hardware.

**CODE PART**

Code part means that has inside that machine level understandable codes. Once we gave our machine level understandable the processer uses for read only. Nothing will write inside that.

**DATA SEGMENT**

It has global variables and static variable.

**BSS**

It has the variables uninitialized and unused variables

**HEAP**

Heap memory use to dynamically store some information.

All Java objects will stored in heap memory only

**STACK**

Stack means first in last and last in first out. Here we storing all our functions, arguments return type, Local variables.