## What is Enum in Java?

Enum – It’s a special class

Enum – Enumeration is a special datatype used to store a collection of constant values that value is set of fixed under one variable name.

An enum in Java is a special class type that represents a group of constants (unchangeable variables, like final variables).

---
## Syntax:
```java
enum Day{  
SUNDAY,MONDAY,TUESDAY  
}
```

Each enum constant as an object of the enum class.

Accessing this enum class you can call directly the class name and use dot. and enum value
```java
Day day = Day.MONDAY;  
System.out.println(day);
```

---
# ENUM METHODS

## 1. values()

values() that returns all the enum constants as an array.

Example:
```java
for (Color c : Color.values()) {  
System.out.println(c);  
}
```

---
## 2. name()

The name() method is a built-in, final method in the java.lang.Enum class.

It returns the exact name of the enum constant as it was declared in the enum — in String form.

Syntax:
```java
enumName.CONSTANT.name();
```

Example:
```java
public class TestEnum {  
public static void main(String[] args) {  
Color c1 = Color.RED;

    System.out.println(c1.name());   // Output: RED  
    System.out.println(Color.GREEN.name()); // Output: GREEN  
}

}
```

---   
## 3. ordinal()  
  
Returns the position of the constant in the enum (starts at 0).  

```java
System.out.println(Color.RED.ordinal()); // 0  
System.out.println(Color.GREEN.ordinal()); // 1  
System.out.println(Color.BLUE.ordinal()); // 2
```
  
---  
## 4. compareTo()  
  
Compares two constants by their ordinal values.  

```java
System.out.println(Color.RED.compareTo(Color.BLUE)); // -2 (0 - 2)  
System.out.println(Color.BLUE.compareTo(Color.GREEN)); // +1 (2 - 1)
```

  Returns:  
  
- Negative → if the first is before the second    
- Zero → if same    
- Positive → if after    
  
---  
  ## 5. equals()  
  
Checks if two enum constants are the same.  

System.out.println(Color.RED.equals(Color.RED)); // true  
System.out.println(Color.RED.equals(Color.BLUE)); // false

  
You can also use == safely because enums are singletons:  

if (Color.RED == Color.RED) { ... } // perfectly safe
  
---  
## 6. toString()  
  
By default, returns the same as name().  
  
But you can override it to provide a custom name or text.  

```java
enum Color {  
RED {  
public String toString() { return "Red Color"; }  
},  
GREEN {  
public String toString() { return "Green Color"; }  
},  
BLUE {  
public String toString() { return "Blue Color"; }  
};  
}

public class TestEnum {  
public static void main(String[] args) {  
System.out.println(Color.RED); // Red Color  
System.out.println(Color.RED.name()); // RED  
}  
}
```

  ---  
## 7. valueOf()  
  
There are two versions:  
  
### Static version (common)  

```java
Color c = Color.valueOf("RED");  
System.out.println(c); // RED
```
  
If the name doesn’t exist, it throws IllegalArgumentException.  
### Generic version  

```java
Color c = Enum.valueOf(Color.class, "BLUE");
```
  
---  
## 8. getDeclaringClass()  
  
Returns the enum’s class type.  

```java
System.out.println(Color.RED.getDeclaringClass());  
// Output: class Color
```
  
Useful in reflection or generic programming.  
  
---  
## 9. hashCode() and getClass()  
  
Inherited from Object:  

```java
System.out.println(Color.RED.hashCode());  
System.out.println(Color.RED.getClass());
```
