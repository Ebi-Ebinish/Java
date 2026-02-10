# Java Datatypes and Variables

## Datatypes

Datatypes are used to specify:

- What type of value a variable can store
- The size of memory required
- They are used while declaring a variable

---
## Java Memory Model

When you run a Java program, memory is mainly divided into two important areas:
### Stack

- Stores method calls and local variables (including references to objects)
- References are like pointers (addresses) that connect variables to objects in the heap
- Fast, temporary memory
- Automatically cleared when a method ends
### Heap

- Stores objects created at runtime using the `new` keyword
- Includes the **String Constant Pool (SCP)** — a special part of the heap for string literals

---
## Note

Primitive datatype storage differs variable-wise.

---
## Types of Variables

### Local Variable

- Stored in **stack memory**
- Exists only while the method is running
- Automatically destroyed when the method ends

### Instance Variable

- Stored in **heap memory**
- Created when an object is created using the `new` keyword
- Each object has its own copy of instance variables
- Heap allows objects to live beyond the method call
### Static Variable

- Stored in the **Method Area**
- Method Area is part of the heap where class metadata is stored

---
## Datatype Categories

1. Primitive
2. Non-Primitive

---
## Primitive Datatypes

- Used to store actual values
- Have a fixed range and limit
- Stored directly in memory
- Examples:
    - `int`
    - `float`
    - `double`
    - `char`
    - `boolean`
    - `short`
    - `long`
    - `byte`

---
## Non-Primitive Datatypes

- Used to store object values
- Size and range do not have a fixed limit
- Examples:
    
    - `String`
    - `Array`
    - `Class`
    - `Object
    - `ArrayList`
---
## String Immutability (Important Note)

String is immutable because every time you modify it, a **new object is created**.

### Example 1: Using `new`

```java
String obj = new String("Hello");
```

- Stored in heap memory
- A new object is created with a new memory address
- `"Hello"` is the object and `obj` is the reference
### Example 2: Using String Literal

```java
String obj = "Hello";
```

- Stored in the **String Constant Pool**
- No new object is created if the same value already exists
- Reference points to the existing object

---
### Reference Assignment

```java
String obj = new String("Hello"); String obj1 = obj;
```

- Using `==` operator:
    - Compares memory addresses
    - Result: `true` (same reference)
- Using `.equals()` method:
    
    - Compares actual content
    - Result: `true`

---

## What is a Literal?

A literal is a **fixed value written directly in the code** that represents data.
### Examples

```java
int a = 10;           // Integer literal String name = "Ebinish"; // String literal
```
Every datatype has a literal value when initialized.

---
## String Constant Pool (SCP)

- All string literals like `"Hello"` and `"Java"` are stored in the **String Constant Pool**
- SCP is part of heap memory
- Purpose:
    - Save memory
    - Improve performance by reusing string objects
### Example

```java
String s1 = "Java"; String s2 = "Java";
```

- Both refer to the same object in the String Pool
- Same memory location is shared
---
## Using `new String()`

```java
String s3 = new String("Java");
```

- Creates a new object in heap memory (outside SCP)
- Even if `"Java"` exists in the pool, `new` forces a new object

### Comparison Example

```java
`String s1 = "Java"; 
String s3 = new String("Java");
System.out.println(s1 == s3);      // false (different memory addresses) System.out.println(s1.equals(s3)); // true (same content)`
```

---
## Why Java Uses String Constant Pool?

1. **Memory Efficiency**
    - Reuses existing string objects instead of creating duplicates
2. **Performance**
    - Reduces object creation time
3. **Immutability of Strings**
    - Since strings can’t be changed, sharing them is safe

---
## Byte Datatype

- Range: `-128` to `127`

### Casting Example

```java
	byte num = (byte) 128;
```

- Value wraps around using modulo `256`
- Result: `-128`

---
## HashCode() Method

- `hashCode()` always returns an `int`
- Size of `int`: **32-bit**
- Hash code is **not random**
- It must be consistent and usable as a unique identifier
- Format: **Base-10 (Decimal)**
    - Example values: `700`, `12`, `1`
- Always within the range of a 32-bit integer