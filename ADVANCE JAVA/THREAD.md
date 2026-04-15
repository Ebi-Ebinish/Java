## What is a Thread?

A thread is like a lightweight subprocess. A Java program always has at least one thread — the **main thread** — but you can create more to perform tasks concurrently.

Think of it like:

- One program = one process
- Multiple threads = multiple tasks running inside that process

## Why use Threads?

- Perform multiple tasks simultaneously
- Improve performance (especially for I/O tasks)
- Better CPU utilization
- Background work (e.g., downloading files while UI is active)
#  Why Threads Exist?

Without threads:

- Your program runs **one task at a time** (sequential)

With threads:

- Multiple tasks run **simultaneously (concurrently)**
### Example:

```java
Download file + Play music + UI interaction
```

Without threads → slow & blocked  
With threads → smooth & parallel feel

# How Java Supports Threads

Java has **built-in multithreading support**.

There are **2 main ways to create threads:**

---
##  Method 1: Extending Thread class

```java
class MyThread extends Thread {  
    public void run() {  
        System.out.println("Thread is running");  
    }  
}  
  
public class Main {  
    public static void main(String[] args) {  
        MyThread t = new MyThread();  
        t.start(); // NOT run()  
    }  
}
```

## Important:

 `start()` creates a new thread  
 `run()` is just a normal method call

# What Happens Internally When You Call start()?

This is where things get interesting 
### Step-by-step internal flow:

1. You call:
    t.start();
2. JVM calls **native method**:
    private native void start0();
3. OS creates a **new native thread**
4. JVM registers this thread with:
    - Thread Scheduler
    - Thread Stack
    - Program Counter (PC Register)
5. Then JVM calls:
    run();

 So actual execution happens inside `run()`, but in a **separate call stack**
#  Memory Model of Threads (Internal View)

Each thread has its own:

- **Stack Memory** (local variables)
- **Program Counter**
- **Registers**

But shares:

- **Heap Memory** (objects)
#  Thread Scheduler (Core Concept)

Java does NOT control execution order.

 OS Thread Scheduler decides:

- Which thread runs
- How long it runs
### Types:

- Preemptive scheduling
- Time slicing

 That’s why output is **not predictable**
# Callable vs Runnable

| Feature      | Runnable | Callable |
| ------------ | -------- | -------- |
| Return value | No       | Yes      |
| Exception    | No       |  Yes     |
# Real Internal Architecture

```code
Java Thread  
   ↓  
JVM Thread (Java Thread API)  
   ↓  
Native Thread (OS Thread)  
   ↓  
CPU Execution
```
# Key Takeaways

- Thread = lightweight execution unit
- `start()` creates new thread (via OS)
- Each thread has separate stack
- Shared heap → causes race conditions
- Synchronization solves concurrency issues
- ExecutorService = best practice

# Priority 

In Thread we have concept called priority, what priority means which thread need to execute first and fast in between the multiple threads.

It's will give the suggestion to the scheduler to execute first.

We have,

```java
MaxPriority  = 10
MinPriority =  1
NormPriority =5
```

In that we can set the priority of an thread using setPriority() Method

and also we can get the current priority of an current thread using getPriority()