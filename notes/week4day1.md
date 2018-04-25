# Recursion Examples, Minimax, Selection Sort
##### No Office Hours, Lecture, Lab (4/25 - 4/27) Professor out of town


## Recursion
Reversing an entries in a list

``` python
def iterRevList(list):
    accumulator = [] #accumulator pattern
    
    for ent in list:
        accumulator = ent + accumulator #concatenation
    
    return acccumulator
```
Runs in linear time
What does the recursive reverse list solution look like?

``` python
def recursiveRevList(list):
    #base case is when it is empty
    if len(list) == 0:
        return []
    
    return recursiveRevList(list[1:]) + list[0] #example of concatenation
```
This also runs in linear O(n) time
* Often times recursive functions are less efficient as opposed to iterative examples


### Linear Search

iterative example of Linear Search

``` python
def iterLinearSearch(A, n, i, x):
    while i <= n:
        if A[i] == x:
            return True, i
            
        i+= 1
        
    return False, None
```

recursive example of Linear Search

``` python
def recLinearSearch(A, n, i, x):
    #base case number 1, when we haven't found anything
    
    if i >= n:
        return False, None
        
    if A[i] == x:
        return True, i
    
    return recLinearSearch(A, n, i + 1, x) #makes sure we increment i up to n

```
This also runs in linear time. Recursive function albeit is a little slower
