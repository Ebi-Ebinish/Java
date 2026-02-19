# COLLECTION - LINKED HASHSET

## What is Linked Hashset?

Stores unique elements (no duplicates — like HashSet)  
Maintains insertion order (unlike HashSet)  
Doesn’t maintain the sorting order.  
Null values are allowed only once.  
Empty Strings are allowed only once.  
It inherits Hashset.  
It implements set interface.  

## Internal Working

Internally, it uses a LinkedHashMap.  
That’s why when you add elements, it keeps unique keys (like HashMap),  
And also keeps a linked list connecting them in insertion order.
