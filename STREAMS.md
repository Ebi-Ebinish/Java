# STREAMS

## What are Streams in Java?

Java Streams were introduced in Java 8 as part of the `java.util.stream` package. They represent a sequence of elements that supports functional-style operations like `map`, `filter`, `reduce`, etc., on collections or arrays.

Think of a Stream as a conveyor belt in a factory:

- Data (objects) come one by one on the belt.
- Workers (operations like `filter`, `map`) process them.
- Finally, something is produced at the end (`sum`, `list`, `max`, etc.).

**Important:** A Stream does NOT store data. It just pulls data from a source and processes it on-the-fly.  

Streams are not always faster than Collections.  

- For simple tasks, Collections (loops) are faster.
- For large data & complex tasks, Streams (especially parallel streams) can be faster.

### Where does Stream get the data?

Stream does NOT store data.  
It takes data from the collection you start with.  

Example: Tree, set, list  

```java
list.stream()
```

So the pipeline always starts from some source, which is usually a Collection.

Every Stream has source --> Intermediator --> Terminator. 
### How Stream processes data?

Streams use **lazy evaluation**.

That means:

- It does NOT process data when you write `.filter()` or `.map()`
- It waits until the final operation (like `.toList()`, `.count()`, `.findFirst()`)

This final operation is called a **Terminal Operation**.

Until then → no data moves in the pipeline!
# hy Streams Were Introduced?

Before Java 8, we used:

- for loop
    
- enhanced for loop
    
- Iterator
    

Example:

List<String> names = Arrays.asList("Ram", "Shyam", "Mohan");  
  
for (String name : names) {  
    if (name.startsWith("R")) {  
        System.out.println(name);  
    }  
}

Problems with traditional looping:

1. Code is verbose
    
2. Hard to parallelize
    
3. Focus is on _how_ to do it (iteration logic)
    
4. More boilerplate code
    

Java 8 introduced:

- Lambda expressions
    
- Functional interfaces
    
- Streams API
    

To shift from:

❌ Imperative style →  
✅ Declarative style
