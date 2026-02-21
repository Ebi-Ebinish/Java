# COLLECTION – PRIORITY QUEUE

## What is a PriorityQueue?

A PriorityQueue in Java is a special type of Queue that arranges elements according to their priority rather than their insertion order.

By default, it is implemented as a Min-Heap, meaning the smallest element has the highest priority.

- It allows duplicate values.  
- It does not allow null values.  
- It does not maintain insertion order.  
- Elements are ordered based on their natural ordering or according to a custom Comparator provided at the time of creation.  

---

## Step 2: add() and offer()

Both are used to insert elements.
pq.add(40);  
pq.offer(15);  
System.out.println("After adding elements: " + pq);

### Internal Working:

1. New element is added at end of heap array.  
2. Then “heapify-up” is performed → compare with parent and swap if smaller.  

Output may look like:

After adding elements: [5, 10, 20, 30, 40, 15]

### Heap Tree:
   5
  / \
10   20
/ \ /  
30 40 15

---
## Methods of PriorityQueue

| Method             | Description              | Return Type | Example         | Internal Operation |
| ------------------ | ------------------------ | ----------- | --------------- | ------------------ |
| add(E e)           | Inserts element          | boolean     | pq.add(10)      | heapify-up         |
| offer(E e)         | Inserts element          | boolean     | pq.offer(20)    | heapify-up         |
| peek()             | Head element (no remove) | element     | pq.peek()       | access root        |
| poll()             | Removes head             | element     | pq.poll()       | heapify-down       |
| remove()           | Removes head             | element     | pq.remove()     | heapify-down       |
| remove(Object o)   | Removes given element    | boolean     | pq.remove(30)   | linear + heapify   |
| contains(Object o) | Checks existence         | boolean     | pq.contains(10) | linear search      |
| size()             | Count elements           | int         | pq.size()       | —                  |
| isEmpty()          | Checks if empty          | boolean     | pq.isEmpty()    | —                  |
| clear()            | Removes all              | void        | pq.clear()      | —                  |
| toArray()          | Converts to array        | Object[]    | pq.toArray()    | —                  |

---
# What is a Comparator in Java?

A Comparator in Java is an interface used to define custom sorting or ordering logic for objects.

It tells how two objects should be compared — i.e., which one is “greater,” “smaller,” or “equal.”

---
## Why do we need Comparator?

Normally, Java classes have a default comparison rule (called natural ordering) if they implement Comparable.

For example:

Integer, Double, and String already implement Comparable:

- Integer: smaller number comes first.  
- String: alphabetical (lexicographical) order.  

But if you have:

- Your own class (like Student, Employee, etc.)  
- Or want a different order (like descending instead of ascending)  

Then you use a Comparator.

---
## When to use Comparator?

| Situation | Use |
|-----------|-----|
| You want custom sorting logic | Use Comparator |
| You don’t own the class (can’t modify it) | Use Comparator |
| You need multiple different sort orders | Use Comparator |
| You want to change default ascending → descending | Use Comparator |
