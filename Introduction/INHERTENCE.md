# INHERITANCE

## What is Inheritance?

Deriving a class from the existing one.  
It allows you to create a new class from an existing class, reusing code and extending functionality.

## Types of Inheritance 

1. Single Inheritance  
2. Multilevel Inheritance  
3. Hieratical Inheritance  
4. Hybrid Inheritance  

---

## Single Inheritance

It has one parent or base class, one child class has inherit from that one base class.  
It creates a simple parent-child relationship.

---

## Multilevel Inheritance 

When a parent class has one child class that child class becomes a parent for another child class it’s called Multilevel Inheritance.

---

## Hierarchical Inheritance

Hierarchical inheritance is when multiple classes inherit from a single parent class.  

---

## Multiple inheritance

**Note:** Multiple inheritance is not support in java because of ambiguity Issues.  

Multiple inheritance means a class inherit more than one class.  

Ex:  

```java
class A {
    void show() { System.out.println("A"); }
}
class B {
    void show() { System.out.println("B"); }
}
class C extends A, B { } // ❌ Java does NOT allow this


   A      B
     \    /
      \  /
       C
```

---
## How can I overcome that?

Java allows multiple inheritance through interfaces, which do not have method bodies (before Java 8).

Even with default methods in interfaces (Java 8+), Java requires the programmer to resolve conflicts explicitly.

```java
interface A {
    default void show() { System.out.println("A method"); }
}
interface B {
    default void show() { System.out.println("B method"); }
}
class C implements A, B {
    public void show() {
        A.super.show(); // explicitly choose which method to call
    }
    public static void main(String[] args) {
        C obj = new C();
        obj.show();
    }
}
```

## Why Inheritance are used

### Code Reusability

Instead of rewriting the same code in multiple classes, you write it once in a parent class and reuse it in child classes.