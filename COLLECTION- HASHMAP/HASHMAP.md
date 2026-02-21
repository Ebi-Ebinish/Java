# COLLECTION – HASHMAP

## What is HashMap?

HashMap is a Java Collection that stores data in the form of key–value pairs.
### Key points:

- Keys are unique (cannot repeat).  
- Values can be duplicate.  
- Allows null key (1) and multiple null values.  
- Not synchronized → NOT thread-safe.  
- Stores items based on hashing technique.  

---
## Hidden Tricky Points (Interview GOLD)

✔ 1. HashMap is NOT thread-safe  

Multiple threads may overwrite data → use ConcurrentHashMap.

✔ 2. High collision → performance drop  

If hashCode() is poorly implemented, all keys go to same bucket → becomes a LinkedList → O(n).

✔ 3. Tree-fication happens only if:

- bucket size > 8  
- array size >= 64  

✔ 4. Avoid mutable keys  

If key changes after insertion → you will never find it again.

Example: using a mutable object as key → BAD.

✔ 5. Order is NOT guaranteed  

HashMap is unordered.

Use LinkedHashMap if you want insertion order.