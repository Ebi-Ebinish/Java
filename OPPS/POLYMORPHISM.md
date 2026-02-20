# METHOD OVERLOADING AND METHOD OVERRIDING

## What is Number in Java?
- Number is a class in `java.lang` package  
- It is the abstract superclass for all numeric wrapper classes in Java:  
  - `Integer`, `Double`, `Float`, `Long`, `Short`, `Byte`  
  - `BigDecimal`, `BigInteger` (also extend Number)  
- So, if a method accepts a Number, it can accept any numeric type object (`Integer`, `Double`, etc.).

## What is Object in Java?
- In Java, Object is a class.  
- It is the superclass of all classes in Java. Every class in Java (directly or indirectly) inherits from `java.lang.Object`.  
- This means you can assign any type of object (`String`, `Integer`, custom class, etc.) to a variable of type `Object`.

## What is Method Overloading?
- Method overloading is in a same class two or more methods with the same name and different types of parameter.  
- It’s also called **compile time polymorphism**.  
- The access modifier can’t be a matter; it can be anything, no restriction.  
- If the return type only differs, the compiler will throw an error.  
- The parameter name (`a` or `b`) doesn’t matter — only the type and number of parameters are considered.

### Why we are calling compile time polymorphism
- Decision made at compile time.  
- The JVM doesn’t need to figure it out at runtime — the compiler already decides and fixes the method call in the bytecode.

### Ambiguity issue
- If the methods have more matches, the compiler will throw ambiguity issue because it can’t identify.  

**Example:**

```java
java id="method-overload-example"
class Methodoverloading {
    public void test(long a, int b){
        System.out.println(a + b);
    }
    
    public void test(int a, long b){
        System.out.println(a + b);
    }
}

// Usage
Methodoverloading a = new Methodoverloading();
a.test(10, 20); // Ambiguous, compiler cannot decide
a.test(10L, 9); // Correct usage
```

## What is Method Overriding?

- Same name
- Same parameter list (signature)
- Same or compatible return type (covariant return is allowed)
- Not less accessible (access modifier cannot be more restrictive than the parent’s).

**Why?**  
Method overriding happens when a subclass provides its own implementation of a method that is already defined in its parent (superclass).