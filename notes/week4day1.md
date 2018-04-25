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
* What does the recursive reverse list solution look like?

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


## Minimax
Tic tac toe is a 2 player, perfect information game. This is a deterministic game, and the game is considered to be solved when there are 3 consecutives Xs and Os.

* Make all the best calls for computer against human

``` python
minimax(board, player)


```
* X = computer
* O = human
    * try to maximize the score for computer
1. Base case  - when computer wins (1)
2. Base case - when human wins (-1)
3. Base case - when draw occurs (0)

Try to maximize computer, minimize human

### Using recursion!
* The base case occurs when we have a full board

computerTurn() -- this is the top level recursive function to determine the best move
* calls minimax, and takes the max value, or best position

Test cases are written when the correct value is returned for the board state


