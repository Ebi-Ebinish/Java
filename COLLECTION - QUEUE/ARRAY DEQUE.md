# COLLECTION – ARRAY DEQUE

## What is array deque?

ArrayDeque (Array Double-Ended Queue) is a resizable array implementation of the Deque interface, which allows elements to be added or removed from both ends efficiently.

- Implements Deque Interface  
- Supports both Queue (FIFO) and Stack (LIFO) operations.  
- Resizable Array  
- Automatically grows when it becomes full.  
- Faster than LinkedList  
- Especially for add/remove operations at both ends.  
- No Capacity Restriction  
- Expands as needed (unlike fixed queues).  
- No Null Elements Allowed  
- Inserting null throws NullPointerException.  
- Not Thread-Safe  
- For multi-threaded environments, use ConcurrentLinkedDeque.  
- Implements Cloneable and Serializable  
- Can be cloned and serialized.  

## What is array deque?

ArrayDeque (Array Double Ended Queue) is a resizable array implementation of the Deque interface.

It supports adding and removing elements from both ends — front and rear.

It was introduced in Java 1.6 and is part of the java.util package.

It doesn’t allow null value.

It allows duplicates

## Why use ArrayDeque?

It can act as:

- Queue (FIFO) – like a normal queue  
- Stack (LIFO) – alternative to Stack class (which is older and synchronized)  

Faster than both:

- Stack (because no synchronization overhead)  
- LinkedList (because no node object allocation)  