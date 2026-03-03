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

