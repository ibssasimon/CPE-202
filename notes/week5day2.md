# Mergesort (Cont), Quicksort


## Merge sort (cont)
* Ran in O(nlogn) time. We must implement a merge function to merge the two recursively sorted lists.

* Merge Function:
``` python
seq [i] < seq[j]
#Swap the two
```

## Quicksort
* Runs in O(nlogn) in the average case
* In it's worse case runs O(n^2)

Number of partitions in the worst case is n.
* The pivot is some number where all the numbers less than pivot, go into the left side of array, and numbers greater than pivot go to the right side of the array
* Another example of a divide and conquer algorithm. The 'divide' runs in O(logn)

Quicksort recursively divides the list into subarrays and partition until you reach base case

``` python
#base case

if len(seq) < 2:
    return seq

```

### Partitioning the array

``` python
pivot = seq[0]
less = [ent for ent in seq[1:] if ent < pivot]
greater = [ent for ent in seq[1:] if ent >= pivot]
return quicksort(less) + pivot + quicksort(greater)
```
## Abstract Data Types

### LinkedLists
``` python
class LinkedLists:
    class __Node :
    #this makes the constructor for node private

```

Inserting at the front of a pyhon list is O(n). Inserting for a linkedlist is constant

### Doubly Linked List
* Adds one extra field to the nodes, where it points to next & **previous**


### Stack
Node points to top and next. 

