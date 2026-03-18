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
# 2. Why Threads Exist?

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