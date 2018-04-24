# Activation Records, Run-Time Stack and Heap, Recursion

## Activation Records
* Basically a record of all the variables defined in a program

Memory is divided into 2 sections

* The Run-Time Stack ( stacked on top of eachother)
* The Heap (described as a cloud where objects are stored)

``` python
xval = '20'
def someFunction(p1):
    xval = '-20'
    return p1 + xval
    
res = someFunction('20') # result = 0

```
Stack (MODULE RECORD)
* xval = '20'
* someFunction
* res
----
* xval = '-20' (SOME FUNCTION RECORD)
* p1


Heap
* object that hold variables

Popped off the stack - when the reference to the variable gets deleted by the garbage collection
* This gets called when a function returns a value

### Stack
* Last in First Out Data Structure
LIFO
* push() - putting item to a stack
* pop() - taking item off a stack



## Recursion
* A self calling function

Example of an infinite recursive function, needs a base case
``` python
def countdown(n):
    if n == 0:
        return
    else:
        print(n)
        countdown(n-1)
```
* Recursive stopping condition is called a *base case*
    * You can turn a recursive problem into non recursive w/ using a stack
    
    
    ## Minimax
1. Decide on the name and the parameters of our function
2. Define a base case

``` python
minmax(player, gamestate)
computerTurn()

```
returns the value (rating) for a gamestate for the player parameter




