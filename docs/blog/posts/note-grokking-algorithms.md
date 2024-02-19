---
date: 2024-02-19
authors:
  - almightyPush
categories:
  - Note
  - Algorithm
---

# Note: Grokking Algorithms

This is my note for the book grokking algorithms. It is really a nice book. It gives most of the fundamental concepts in simple terms. My number one recommendation for any one who is starting data stractures and algorithms.

<!-- more -->

## Big O notation

A notation that tells you how fast an algorithm run. It doesn’t tell you how long it will take but it gives you the number of operations it will need to perform for the worst case scenario. This is particularly useful when number of items increase. 

Common Big O run times

- `O(1)` constant time - Reading array
- `O(log n)` log time - Binary search
- `O(n)` linear time  - Simple search
- `O(n * log n)` -
- `O(n²)` exponential time - selection sort
- `O(n!)` factorial time - The traveling sales person

Algorithm speed isn’t measured in seconds, but in growth of the number of operations. Instead, we talk about how quickly the run time of an algorithm increases as the size of the input increases.

`O(log n)` is faster than`O(n)`, but it gets a lot faster as the list of items you are searching grows. 

## Binary Search

**Input:** a sorted list of items

**Big O:** `O(log n)`

**Return:** position of item else NULL

**Steps**

- Check if the middle items is what you are looking for
    - If target is greater than middle look into items to the right of the middle value
    - if target is less than the middle value look into items to the left of the middle value
- Do the above operation when looking for a target in any subset of the items until target is found or run out of items to look into.

```
SET items to list of sorted items
SET low to zero
SET high to number of items - 1  // if zero based indexing

INPUT target

WHILE low <= high
	
	SET mid to (low + high) / 2 rounded down
	
	IF item at position mid equals target THEN
		OUTPUT mid
	ELSE IF item at position mid is less than target THEN
		SET high to mid - 1
	ELSE
		SET low to mid + 1
	ENDIF

ENDWHILE

OUTPUT NULL  // return null if target not in list
```

## Array vs Linked List 

| Array     | Linked List |
| --------- | ----------- |
| finite items consecutively in memory | infinite items randomly in memory, item address linked to previous item |
| Stores finite items in a memory next to each other | Stores infinite items in a memory randomly |
| Once created, additional items can not be added | Additional items can be added after creation |
| It is `O(1)` to access an item, `O(n)` to insert an item & `O(n)` to delete an item | It is `O(n)` to access an item, `O(1)` to insert an item & `O(1)` to delete an item |
| Suitable for lots of reads and few inserts | We assume the position to insert into and deletion from is known |
| Random access, this makes array the most used | Sequential access |
| All items should be the same type | Items can be different types |


## Selection sort

**Input:** a list of items

**Big O:** `O(n²)`

**Return:** sorted items

**Steps**

- Go through the list of items and take out the smallest value
- Repeat this until all items have been sorted
