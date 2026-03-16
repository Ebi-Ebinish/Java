# What is lambda Expression

It's use provide a implementation for the functional interface in a short way.

before java 8 
## Normal Object Creation (Before Lambda)

When you implement a functional interface using an **anonymous class**, Java **creates a separate class file internally**.

Example:

```java
interface MyInterface {  
    void display();  
}  
  
public class Test {  
    public static void main(String[] args) {  
  
        MyInterface obj = new MyInterface() {  
            public void display() {  
                System.out.println("Hello");  
            }  
        };  
  
        obj.display();  
    }  
}
```

# Lambda Expression (Java 8+)

Example:

```java
MyInterface obj = () -> System.out.println("Hello");
```

### Internally what happens

Java **does NOT create a separate anonymous class file** like before.

Instead, Java uses:

### **`invokedynamic` instruction + LambdaMetaFactory**