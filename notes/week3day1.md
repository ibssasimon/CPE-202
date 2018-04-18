# Big-Oh Notation examples, Scope, Recursion, Stack & Heap

## Common Complexities
where T(n) represents a cost function
* O(1) - constant, T(n) = C
* O(logn)  - logarithmic
* O(n) - linear, T(n) = 0.05n + 70,000
    * Note, look at the leading term of equation
* O(nlogn) - slightly faster than O(n)
* O(n^c) - polynomial
* O(C^c) - exponential

### Profile curve of common complexities
* (See notebook for image of curves)


## How many operations?
### Constant Time
``` python
def add2Numbers(a, b):
    return a + b
    #One add operation
    
def add3Numbers(a, b, c):
    return a + b + c
    #2 additions
    
```
As params get larger, operations get larger.
* T(n) = 1
* T(n) = 2


### Linear Complexity

```python

def addNumbers(list):
    total = 0
    for entry in list:
        total += entry
    return total
```
Cost function: T(n) = n - 1. We get n-1 because there is one less add than there are numbers in a list
T(n) is in set of O(n)

``` python

def findAvgOfNNumbers(list):
    total = addNumbers(list)
    
    return total / len(list)
```
T(n) = (n -1 ) + n + 1
T(n) = 2n + c

Professor is concerned with complexity class of algorithm.


### Sorting Algorithm
count on comparisons per inner loop iteration (n - 1)
* Sorting low to high
    * O(n^2)
    
``` python

def bubbleSort(list):
    i = 1
    while i < len(list) - 1:
        idx = 0
        
        while idx < len(list) - i:
            if list[idx] > list[idx + 1]:
                temp = list[idx] #Swapping part of algorithm
                list[idx] = list[idx + 1]
                list[idx + 1] = temp
            idx += 1
```
Cost function: all about comparison operation! (If statements)

T(n) = summation (n - i ), i = 1 -> n-1

(n - 1) + (n - 2) + . . . + 0

n * O(n)  is a set of O(n^2)
average case  = O(n^2)
best case = O(n)


## Scope
``` python
tval = 7 # module / global scope
xval = 0
xval = 1
def func1(zval):
    xval = 2 # local scope
    yval = 3
    
    def func2(aval):
        bval = 5
        print(aval)
        print(xval)
        print(tval)
    
    func2(10)

```
func2 is considered a local variable of func1

### Scope levels
* local
* enclosed
* global
* built-in

