# GENERICS

## What is Generic?
- Java is a type safety programming language.
- To avoid the run time class cast Exception  
- `ArrayList obj = new ArrayList();` → Raw Type of storing the elements in the list.
- In java 1.2 we have collection API
- In java 1.5 we have the generic for type define 

## What is Autoboxing in Java?
Autoboxing is a Java feature where the compiler automatically converts a primitive data type into its corresponding wrapper class object.  
It was introduced in Java 5.

## What generics actually do (very important)
- Generics do NOT change runtime behavior.
- They work only at compile time.
- Generics fix this problem by letting you tell the compiler: "This list will only hold Strings" or "This list will only hold Integers". The compiler checks everything while you write the code and gives an error immediately if you try to put the wrong type.
- `E` it means it’s an element.
- `T` is called a type parameter. It's like a variable for types
- `?` - Wildcards

### Wildcard
Wildcard is unknown type  

```java
void printList(List<?> list) {
    // works with any kind of list
}

```

### **Limitation:**

- You cannot add elements (except null)

```java
list.add("Hello"); // not allowed
```

Because Java doesn’t know the exact type. Java doesn’t know which type of request your passing to add an element.  
You can add the null element only.

### Wildcard Example

Imagine you have these two lists:

```java
List<String> stringList = new ArrayList<>();
stringList.add("Apple");
stringList.add("Banana");

List<Integer> numberList = new ArrayList<>();
numberList.add(10);
numberList.add(20);
```

You want to write one method that can print any list — whether it's a list of strings, integers, or anything else.

**What is a Wildcard?**  
The symbol `?` means "unknown type".  
So `List<?>` means: "a list of some unknown type".

**Important Rule with Wildcards:**

**You Can Read, But You Cannot Add**  
When you use `List<?>`, Java says:

- You can read items (as Object).
- But you cannot add anything (except null).

Why this restriction? Because Java doesn't know what exact type the list holds. It could be List, so adding an Integer would be dangerous.

## Three Types of Wildcards

1. **Unbounded Wildcard: ?**
    
    - Meaning: Any type.
    
    - Use when: You only want to read from the list (not add).
    
    - Example: Printing, counting size, etc.
    
```java
void printSize(List list) {
    System.out.println("Size: " + list.size()); 
}
```

2. **Upper-Bounded Wildcard:**  
There is NO common upper bound (except Object):

```java
Object
 ├── Number
 │    └── Integer
 └── String
```

