In imperative you control everything 
1. flow
2. state 
3. Iteration 
4. execution steps 
### Example
```java
List<String> result = new ArrayList<>();

for (String name : names) {
    if (name.startsWith("A")) {
        result.add(name.toUpperCase());
    }
}
```
### What is happening technically?

- You allocate a mutable list (`result`)
- You create an external iterator (`for`)
- You control loop execution
- You mutate state (`result.add`)
- You define the algorithm step-by-step

## You are responsible for:

- Order of execution
- State changes
- Loop termination
- Side effects

This is **imperative control flow**.

# DECLARATIVE

In declarative you avoid the above the thinks.
# Example (Stream)
```java
List<String> result = names.stream()
    .filter(n -> n.startsWith("A"))
    .map(String::toUpperCase)
    .toList();
```

### What is happening technically?

You define:

- A pipeline of **stateless operations**
- Functional transformations (`filter`, `map`)
- A terminal operation (`toList()`)

## You do NOT define:

- How iteration occurs
- How elements are stored internally
- When exactly each step executes
- Whether execution is sequential or parallel    

## The Stream API manages:

- Internal iteration
- Laziness
- Optimization
- Potential parallel execution

This is **declarative data processing**.

## The final thinks is Stream are declarative 

