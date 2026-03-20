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