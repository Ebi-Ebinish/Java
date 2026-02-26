# What is Functional Interface?

* The functional interface has only one abstract method.
* Or multiple static method 
* Or multiple default method

Even if you don’t write `@FunctionalInterface`, it is still functional —  
that annotation just tells the compiler to check the rule.
### From Java 8:


```java
@FunctionalInterface  
public interface MyInterface {  
    void show();   // Only one abstract method  
}
```

This is valid.

Even this is valid:

```java
@FunctionalInterface  
public interface MyInterface {  
    void show();   // One abstract method  
  
    default void display() {  
        System.out.println("Default method");  
    }  
  
    static void print() {  
        System.out.println("Static method");  
    }  
}
```

Still functional interface   
Because only **one abstract method** exists.
## What if there are two abstract methods?

```java
public interface MyInterface {  
    void show();  
    void display();  
}
```

❌ This is NOT a functional interface.

#### Functional Interface With multiple static and default methods

```java
@FunctionalInterface  
interface MyFunctionalInterface {  
  
    //  Only ONE abstract method  
    void execute();  
  
    //  Multiple default methods allowed  
    default void method1() {  
        System.out.println("Default Method 1");  
    }  
  
    default void method2() {  
        System.out.println("Default Method 2");  
    }  
  
    //  Multiple static methods allowed  
    static void staticMethod1() {  
        System.out.println("Static Method 1");  
    }  
  
    static void staticMethod2() {  
        System.out.println("Static Method 2");  
    }  
}
```

✔ This is still a **valid functional interface**  
Because only **one abstract method** exists.

# Tricky Things About Functional Interface
# What Exactly Is a Functional Interface?

A **Functional Interface** is:

> An interface that has **exactly one abstract method**.

That’s the official definition.

Example:

```java
@FunctionalInterface  
interface MyFunctionalInterface {  
    void execute();  
}
```

Even if you don’t write `@FunctionalInterface`, it is still functional —  
that annotation just tells the compiler to check the rule.

