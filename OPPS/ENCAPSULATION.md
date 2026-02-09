
# ENCAPSULATION

## What is Encapsulation?
Encapsulation is hiding the information showing the functionality.

## Real-Life Example
**ATM Machine**  
You don’t directly touch the bank’s database (balance variable).  
You interact via buttons (methods like `withdraw()`, `deposit()`).

## Purposes
- Mainly used for data protection.
- Controlled Access (Read/Write rules)

Encapsulation lets you decide:
- A field can be read-only (getter only).
- A field can be write-only (setter only).
- A field can be read/write (both).

## Validation & Business Rules
Encapsulation allows putting logic inside setters/getters.

**Example: Prevent invalid age**
```java
class Student {
    private int age;

    public void setAge(int age) {
        if(age >= 5 && age <= 100) this.age = age;
        else System.out.println("Invalid Age!");
    }
}
```

## Data security

Encapsulation allows you to hide internal data and control access, and by giving only a setter without a getter, you hide the data entirely so it can only be set but never retrieved externally — increasing security.

## Inner class

A class that as inside another class that is inner class. It has a group of class.  
Used in encapsulation for accessing the private member.  
Used in event Handing and call-backs, etc.

## Types of Inner class

1. Non-static inner class
2. Static nested class
3. Local inner class
4. Anonymous inner class

---
## Non-Static Inner class

A class defined inside another class, not marked as static. Requires an instance of the outer class to create.
### Example of Non-static Inner Class

```java
class Outer {
    private int outerValue = 10;
    class Inner {
        void display() {
            System.out.println("Outer value: " + outerValue); // Can access outer class's private members
        }
    }
    void createInner() {
        Inner inner = new Inner();
        inner.display();
    }
}z
public class Test {
    pulic static void main(String[] args) {
        Outer outer = new Outer();
        Outer.Inner inner = outer.new Inner(); // Instance of inner class
        inner.display();
    }
}

```

Inner class can access private fields of outer class.  
To create an inner class object, we need an outer class object.
## Static Nested class

A class defined inside another class and marked as static. Doesn’t require an instance of the outer class.

# Example of Static Nested Class

```java
class Outer {
    static int outerValue = 20;
    static class Nested {
        void display() {
            System.out.println("Outer value: " + outerValue);
        }
    }
}
public class Test {
    public static void main(String[] args) {
        Outer.Nested nested = new Outer.Nested();
        nested.display();
    }
}

```

Static nested classes cannot access non-static members of outer class directly.  
No outer class object needed.
## Local Inner class

A class defined inside a method of the outer class.

### Example of Local Inner Class

```java
class Outer {
    void myMethod() {
        int localVar = 50;

        class LocalInner {
            void display() {
                System.out.println("Local variable: " + localVar);
            }
        }

        LocalInner inner = new LocalInner();
        inner.display();
    }
}

public class Test {
    public static void main(String[] args) {
        Outer outer = new Outer();
        outer.myMethod();
    }
}

```

Local inner classes can only access final or effectively final local variables.

## Anonymous Inner class

A class without a name, defined and instantiated in one place, usually to override a method.

### Example of Anonymous Inner Class

```java
abstract class Greeting {
    abstract void sayHello();
}

public class Test {
    public static void main(String[] args) {
        Greeting greeting = new Greeting() {
            void sayHello() {
                System.out.println("Hello from anonymous inner class!");
            }
        };

        greeting.sayHello();
    }
}

```

Anonymous inner classes are used when you need to override a class or interface method instantly without writing a separate class.