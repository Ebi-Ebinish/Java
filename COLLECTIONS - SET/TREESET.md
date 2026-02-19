## What is treeset?

A TreeSet in Java is a sorted, unique collection of elements.  
It is part of the java.util package and implements the NavigableSet interface.  
A TreeSet stores elements in sorted order (ascending by default) and does not allow duplicates.  

It doesn’t allow to store a null value  
It allow to store empty string.  

A TreeSet uses comparison, not hashing.  

## Tree set uses Tree Map

Internally, TreeSet is built on top of a TreeMap — just like HashSet uses a HashMap.  
Each element you add to a TreeSet becomes a key in a TreeMap.  
The values are a dummy constant object (just like PRESENT in HashSet).  
The TreeMap internally uses a Red-Black Tree (a self-balancing binary search tree).  

## What is a Red-Black Tree?

A Red-Black Tree is a self-balancing Binary Search Tree (BST) used by TreeMap (and hence TreeSet) to maintain sorted order and O(log n) performance.  

## Structure of a Red-Black Tree Node

```java
class Node {
    int key;
    Node left;
    Node right;
    Node parent;
    boolean color; // RED = true, BLACK = false
}
```

### So, every node has:

- key: the value
- left and right: children
- color: red or black

If you want, I can also format it more professionally for notes or documentation style.
