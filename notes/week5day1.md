# Merge Sort, Quicksort, LinkedLists

#### All sorting algos depend on the ability to have random access in a list

## Mergesort


* Recursive algorithm
    * Divide and conquer (merge on the smaller cases)
    
    
    ``` python
        mid = list[(start + stop) / 2]
    
    ```
    
    1. Divide the problem into a number of sub-problems that are smaller instances of the original problem
    2. Conquer the sub-problems by solving them recursively. If they are small enough, solve the problems as a base case
    3. Combine the solutions to the sub-problems into the solution for the original problem (where we merge)
    
``` python
    merge (list, start, mid, stop)
```






