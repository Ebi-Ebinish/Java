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

# Tricky Things About Functional Interface

This is where most developers get confused.
## ✅ Trick #1: Object class methods don’t count

Example:

```java
@FunctionalInterface  
interface Test {  
    void run();  
  
    boolean equals(Object obj);  // From Object class  
}
```

Still valid ✅

Because `equals()` is already defined in `java.lang.Object`.

Java ignores Object methods when counting abstract methods.

#  Now the Most Important Part 

# How Object Is Created Internally With Lambda?

This is what many developers don’t know.

Let’s take:

```java
Runnable r = () -> System.out.println("Hello");
```

### Question:

Where is the object created?  
How does it work internally?

---
##  Step 1: Runnable is Functional Interface

```java
public interface Runnable {  
    void run();  
}
```

Only one abstract method → eligible for lambda.

---
##  Step 2: Compiler Converts Lambda

When you write:

```java
Runnable r = () -> System.out.println("Hello");
```

The compiler internally converts it into something like:

```java
Runnable r = new Runnable() {  
    @Override  
    public void run() {  
        System.out.println("Hello");  
    }  
};
```

BUT ⚠

After Java 8, it is NOT actually creating an anonymous inner class.
### So internally:

1. Compiler sees lambda
2. It checks target type (functional interface)
3. It generates a private synthetic method
4. JVM dynamically creates implementation at runtime
5. That implementation is assigned to reference variable