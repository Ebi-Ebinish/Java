## Array List

- Implemented from List interface.  
- Dynamic sizing: Unlike regular arrays, Array List can grow and shrink automatically as elements are added or removed.  
- Indexed access: Provides fast random access to elements using indices (O(1) time complexity).  
- Ordered: Maintains the insertion order of elements.  
- Allows duplicates: Can store duplicate elements.  
- Allows null: Can contain null values.  
- Not synchronized: Not thread-safe by default (use Collections.synchronizedList() or CopyOnWriteArrayList for thread safety).  

---
## Resizing Process

- Create a new larger array (typically 1.5x the old size)  
- Copy all references from old array to new array  
- Replace the old array with new array  
- Old array becomes eligible for garbage collection  

---
## Memory Area

| Memory Area | What’s inside |
|-------------|--------------|
| Stack | reference variable numbers → points to ArrayList object |
| Heap | ArrayList object with elementData array [ Integer(10), null, null ] |

---
## Disadvantages

### 1. Slow insertions and deletions (especially in the middle)

When you add or remove an element in the middle of the list, all subsequent elements must be shifted.  
This makes insertion/deletion operations O(n) (slow for large lists).

### 2. Memory waste due to dynamic resizing

ArrayList uses an array internally.  
When the array becomes full, it creates a new larger array (usually 50% larger) and copies old elements.  
This resizing and copying cost both time and memory.

---
## Advantages

### 1. Dynamic size (Resizable array)

Unlike normal arrays, the size of an ArrayList grows automatically when elements are added.  
You don’t need to define the size in advance.

### 2. Fast random access (index-based)

Elements are stored contiguously in memory, like arrays.  
Accessing or updating an element by index is O(1) (very fast).

---
## The Methods are

| Method | Purpose |
|--------|----------|
| add(e) | Add element |
| add(index,e) | Insert element at index |
| get(index) | Get element |
| set(index,e) | Replace element |
| remove(index/o) | Remove element |
| clear() | Empty list |
| size() | Get total elements |
| isEmpty() | Check if empty |
| contains(o) | Check element exists |
| indexOf(o) | Get first index |
| lastIndexOf(o) | Get last index |
| toArray() | Convert to array |
| clone() | Copy list |
| ensureCapacity() | Expand memory |
| trimToSize() | Reduce memory |
| subList() | Get part of list |
| iterator() | Iterate safely |
| forEach() | Lambda iteration |
| removeIf() | Conditional delete |
| sort() | Sort elements |
