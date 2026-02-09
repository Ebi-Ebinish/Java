# ABSTRACTION

## What is abstraction?
Abstraction is hiding the implementation of the class and showing the details.  

In words we know what happens,  
But we don’t know how it’s happens  

### Example:
TV remote  

It focuses on what an object does rather than how it does it.

---
## What is Concrete Method in Java?
In Java, a concrete method is a method that has a complete implementation or definition. This means it contains a method body with executable code, unlike an abstract method which only has a declaration and no implementation.

### Key characteristics of concrete methods:
- **Implementation**: They have a defined body enclosed in curly braces `{}`.
- **Instantiability**: They belong to concrete classes (classes that are not abstract) or can exist within abstract classes alongside abstract methods.
- **Inheritance and Overriding**: Concrete methods can be inherited by subclasses and can be overridden if they are not declared as `final`.
- **Execution**: To execute a concrete method, an object of the class containing the method must be instantiated, and the method can then be called on that object.

---
## We can archive abstraction in two ways:
1. Abstraction class  
2. Interface  

---
## Abstraction Class
The class will declared with `abstract` keyword.  

Subclasses must implement abstract methods.  

The class can have both abstract methods and concrete methods.  

Cannot create object directly using `new` keyword.

### Example:
```java
abstract class Animal {
    public abstract void makeSound();
}
```

### Why?

Because `Animal` is abstract — it's incomplete. It may have abstract methods (without a body), so Java doesn’t allow creating an instance of it.

---
## If I have concrete method inside abstract class that time can I access directly using object new keyword?

No, you cannot create an object of an abstract class (even if it contains concrete methods), so you cannot access any methods directly using `new` keyword.

An abstract class is like a partial blueprint. If it has abstract methods, those methods don’t have any implementation.

Java says:  
"You can't build (instantiate) something with missing parts."

Abstract classes are designed to be extended, not used directly. They're like templates meant to be filled in by subclasses.

It’s compulsory to override an abstract method in a subclass.

---
## Interface

An interface is a blueprint of a class.

It defines a set of methods that class must be implemented.

Interfaces provide abstraction (only method signatures, no implementation).

Classes that implement the interface provide their own version of the behavior.

---
## Characteristics of Interface

By default, all methods inside an interface are:

- `public`
- `abstract` (before Java 8)
#### From Java 8 onwards:
- Can also contain `default` and `static` methods.

### From Java 9 onwards:

- Can contain `private` methods as helper methods.

Variables in an interface are:

- `public static final` (constants) by default.

Interfaces cannot be instantiated (like abstract classes).

Only classes implementing the interface can create objects.

A class can implement multiple interfaces → Java’s way of achieving multiple inheritance.

Example:

```java
// Step 1: Define an interface
interface Vehicle {
    void start();   // abstract method (no body)
    void stop();    // abstract method (no body)
}

// Step 2: Car implements the interface
class Car implements Vehicle {
    public void start() {
        System.out.println("Car starts with key");
    }

    public void stop() {
        System.out.println("Car stops with brake");
    }
}

// Step 3: Bike implements the interface
class Bike implements Vehicle {
    public void start() {
        System.out.println("Bike starts with self-start button");
    }

    public void stop() {
        System.out.println("Bike stops with disc brake");
    }
}

// Step 4: Test the abstraction
public class Main {
    public static void main(String[] args) {
        Vehicle v1 = new Car();   // upcasting
        v1.start();              // Car starts with key
        v1.stop();               // Car stops with brake

        Vehicle v2 = new Bike();
        v2.start();              // Bike starts with self-start button
        v2.stop();               // Bike stops with disc brake
    }
}
```

## Tricky points

- Abstract class will have constructor.
### Abstract Methods Can’t Be `private`, `static`, or `final`

Because:

- `private` → can’t be overridden
- `final` → can’t be overridden
- `static` → belongs to class, not object

And abstract methods must be overridden, so these modifiers make no sense.

---
## Interface (Additional Points)

- Variables are always `public static final` (Constants).
- Interface can extend multiple interfaces.
- Static methods can be called only using the interface name, not through implementing classes.

---
## Interface and Abstraction differences

|Interface|Abstraction|
|---|---|
|Enforce to implements abstract method to be defined in interface which is does not have relationship (Relationship means – Each interface and its class have their own set of rules).|Abstraction could be links between two classes which can share their things like Inheritance and it make sensible relationship|

### Points:

1. According to interface, enforce to implements abstract method to be defined in interface which is does not have relationship (Relationship means – Each interface and its class have their own set of rules).
2. Abstraction could be links between two classes which can share their things like Inheritance and it make sensible relationship.
