LinkedList is a data structure that stores elements as a chain of nodes  
each node contains the data and links (pointers) to the previous and next nodes.  

- List interface → behaves like a list (ordered collection)  
- Deque interface → behaves like a queue (supports addFirst, addLast, etc.)1  

Each element (node) contains three parts:  
- The data  
- A reference to the next node  
- A reference to the previous node  

---
## Performance

- Fast insertions/deletions at the beginning or end: O(1)  
- Fast insertions/deletions in the middle (if you have the position): O(1)  
- Slow random access: O(n) - must traverse from the beginning or end  
- More memory overhead than ArrayList due to storing references  

---
## How Operations Work

### Add Operation

When you do `list.add(4)`:

- A new node is created (newNode)  
- The next pointer of last node points to newNode  
- The prev pointer of newNode points to the old last node  
- last reference is updated  

Time Complexity: O(1)

---
### Get Operation (`list.get(3)`)

Starts from head and traverses node by node until it reaches the 3rd node.  

- If index is near start → traverses forward  
- If index is near end → traverses backward  

Time Complexity: O(n)

---
### Remove Operation

When you remove an element:

- It adjusts the next and prev pointers of neighboring nodes  
- No shifting of elements like in ArrayList  

Time Complexity:  
- Remove first/last → O(1)  
- Remove middle → O(n) (because you must reach that node)  

---
## Insertion Methods

| Method | Description | Example |
|--------|------------|----------|
| void addFirst(E e) | Adds element at beginning. | list.addFirst("Start"); |
| void addLast(E e) | Adds element at end. | list.addLast("End"); |
| boolean offer(E e) | Adds at tail (like add). | list.offer("Data"); |
| boolean offerFirst(E e) | Adds at head, returns true/false. | list.offerFirst("A"); |
| boolean offerLast(E e) | Adds at tail, returns true/false. | list.offerLast("Z"); |
| void push(E e) | Pushes onto stack (same as addFirst). | list.push("Top"); |

---
## Retrieval Methods (No Removal)

| Method | Description | Example |
|--------|------------|----------|
| E getFirst() | Gets first element (throws exception if empty). | list.getFirst(); |
| E getLast() | Gets last element. | list.getLast(); |
| E peek() | Retrieves head (null if empty). | list.peek(); |
| E peekFirst() | Retrieves first element (null if empty). | list.peekFirst(); |
| E peekLast() | Retrieves last element (null if empty). | list.peekLast(); |

---
## Removal Methods

| Method | Description | Example |
|--------|------------|----------|
| E remove() | Removes head element (throws exception if empty). | list.remove(); |
| E removeFirst() | Removes first element. | list.removeFirst(); |
| E removeLast() | Removes last element. | list.removeLast(); |
| E poll() | Removes head, returns null if empty. | list.poll(); |
| E pollFirst() | Removes first element (returns null if empty). | list.pollFirst(); |
| E pollLast() | Removes last element (returns null if empty). | list.pollLast(); |
| E pop() | Pops from stack (removes first). | list.pop(); |
| boolean removeFirstOccurrence(Object o) | Removes first occurrence of given object. | list.removeFirstOccurrence("A"); |
| boolean removeLastOccurrence(Object o) | Removes last occurrence. | list.removeLastOccurrence("B"); |
