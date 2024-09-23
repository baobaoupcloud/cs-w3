---
title : "Searching algorithms"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
**Searching algorithms** are procedures used to find a specific item or element within a collection of data. 

We will go through two commonly used searching algorithms: ***linear search*** and ***binary search***

#### Linear search

In this algorithm, to search a specific item, each element in the collection is sequentially checked until the desired item is found, or the entire list is traversed. The time complexity is O(n). It is suitable for small-sized or unsorted lists. 

Below is the pseudocode for linear search algorithm to find the number 50 behind the lockers doors:

```bash
For i from 0 to n-1
    If 50 is behind doors[i]
        Return true
Return false
```

#### Binary search

This algorithm is applicable only to sorted lists. It repeatedly breaks the list into halves and compares the middle element of the list with the target element, then narrows down the search range to the left or right half from the comparison result. The time complexity is O(log n). It is highly efficient when searching large sorted lists.

Below is the pseudocode for binary search to find the number 50 behind the lockers doors:

```bash
If no doors left
    Return false
If 50 is behind middle door
    Return true
Else if 50 < middle door
    Search left half
Else if 50 > middle door
    Search right half
```