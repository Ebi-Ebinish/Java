# COLLECTION – HASHSET

## What is Hashset?

Hashset is a collection framework that implements a set interface.  
It doesn’t allow to store a duplicate values  
It allow null value.  
It doesn’t maintain the insertion order  
Internally hashset uses Hashmap.  
It doesn’t add the value like sorted format.  
The index based access will not be worked here.  

## HashSet uses HashMap

When you call add("Apple"):

The hashCode() of "Apple" is computed.  
The hash is used to find the bucket in the HashMap.  
If no element with that hash exists → added successfully.  
If a matching key (based on equals()) exists → ignored.  

When you call add("Apple") again:

The same hash and equals check finds the key already exists.  
So, no duplicate is added.  

## Resizing (rehash)

When size > capacity * loadFactor (default: size > 16 * 0.75 = 12), the table doubles to 32.  
Every existing entry must be reinserted into the new table (index depends on new capacity).  
Resizing is expensive (O(n)) but amortized over many inserts.
