# COLLECTION – QUEUE

## What is Queue?

A Queue in Java is a linear data structure that follows the FIFO (First In, First Out) principle.

That means:

The element that is inserted first will be removed first.

It’s just like a real-life queue (line) — for example, people waiting in line at a ticket counter.

The person who comes first gets served first.

---
## Common Implementations of Queue

| Implementation | Description | Ordering | Allows Null? | Thread Safe? |
|---------------|------------|----------|--------------|--------------|
| LinkedList | Implements both List and Queue | FIFO | ✅ Yes | ❌ No |
| PriorityQueue | Orders elements based on priority (natural/comparator) | Priority order | ❌ No | ❌ No |
| ArrayDeque | Resizable array-based deque | FIFO/LIFO (double-ended) | ❌ No | ❌ No |
| ConcurrentLinkedQueue | Thread-safe queue for concurrency | FIFO | ❌ No | ✅ Yes |
| BlockingQueue (interface) | Used in multithreading (e.g., Producer-Consumer) | FIFO or Priority | ❌ No | ✅ Yes |
