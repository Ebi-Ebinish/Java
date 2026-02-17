
Constructor is class name the method name are same.  
It doesn’t return anything. Doesn’t have return type.  
It automatically called when the object is created using new keyword.  

## Types
1. Default constructor  
2. Parameterized constructor  
3. Copy constructor  

---
## Default Constructor
The constructor doesn’t have parameter it is called copy constructor.  
If you don’t write any constructor java automatically provides a default constructor.  

---
## Parameterized Constructor
A constructor will have parameters that is called parameterized constructor.  

---
## Copy Constructor
A constructor will copy values from another object that is called copy constructor.  

Ex:  
```java
Student obj = new Student(20, “ebi”);
Student obj1 = new Student(obj);   // copy constructor
```

---
## Constructor Overloading
You can overload constructors with different parameters, and the compiler decides which one to call at compile time.

```java
class Test {
    Test() {
        System.out.println("Default constructor");
    }
    Test(int a) {
        System.out.println("Parameterized constructor: " + a);
    }
}

public class Main {
    public static void main(String[] args) {
        new Test();    // calls default
        new Test(10);  // calls parameterized
    }
}
```

---
## Constructor Chaining with this()
You can call one constructor from another inside the same class.  
Must be the first statement in the constructor.

```java
class Test {
    Test() {
        this(100);  // calling another constructor
        System.out.println("Default constructor");
    }
    Test(int a) {
        System.out.println("Parameterized: " + a);
    }
}

public class Main {
    public static void main(String[] args) {
        new Test();  
    }
}
```

---
## This ()

This is a constructor call.  
Call another constructor in the same class.  
Must be first in the constructor body.  

Ex:  
```java
this(100);    // this value will pass to the parameterized constructor.
```

This is called constructor chaining.  

---
## This

It is a keyword. This can be used anywhere inside the class.  

### Referring to Instance Variables
When a local variable or method parameter has the same name as an instance variable, this is used to explicitly refer to the instance variable, resolving the ambiguity.

Ex:

```java
class ThisKey {
    int a = 10;
    
    void test() {
        int a = 100;
        int result = this.a;
        System.out.println(result);
    }
}

public class Main {
    public static void main(String[] args) {
        ThisKey obj = new ThisKey();
        
        obj.test();
        System.out.println("Hello World");
    }
}
```

---
## Super ()

This is a constructor call.  
Calls the parent class constructor.  
Inside the constructor body it must be a first.  
It is called chaining up hierarchy.  

Ex:  
```java
super(100);   // this the value will pass parent class constructor.
```

---
## Super

This is keyword.  
This is used to access a parent class variables and methods.  
You can use anywhere inside a class.  

```java
class Parent {
    int number;
    Parent(int n) {
        number = n;
    }
    void displayParent() {
        System.out.println("Parent number: " + number);
    }
}

class Child extends Parent {
    Child(int n) {
        super(n);
    }
    void show() {
        super.displayParent(); // call parent method
        System.out.println("Child can also use number = " + super.number);
    }
}

public class Main {
    public static void main(String[] args) {
        Child c = new Child(100);
        c.show();
    }
}
```

---
## Comparison Table

| Feature | Default Constructor | Parameterized Constructor | Copy Constructor |
|----------|----------------------|----------------------------|------------------|
| Arguments | No | Yes (custom values) | Yes (an object of same class) |
| Purpose | Initializes with default values | Initializes with user-given values | Creates a new object as a copy of another |
| Provided by Compiler? | Yes (if no constructor is defined) | ❌ No, must define | ❌ No, must define manually |
| Example Usage | new Student(); | new Student("John", 22); | new Student(existingStudent); |
| Values set | Default values (e.g., null, 0, etc.) | Provided by user | Copied from another object |
