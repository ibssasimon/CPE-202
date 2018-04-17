# XML & Big-Oh Notation

## XML Parser
Using minidom --

```python
graphicsCommands = xmldoc.getElementsByTagName("GraphicsCommands")[0]

for commandElement in graphicsCommands:
    command = commandElement.firstChild.data.strip()
    attr = commandElement.attributes
    
    if command == "GoTo":
        x = attr["x"]
        x = float(x)
```
Values in attribues are objects that have a property called 'value'


## Accessing Memory in List
* Accessing memory always has O(1) runtime
    * Random Access Memory - Always running constant.

```python
x = [1, 2, 3, 4, 20]
y = ["Simon", "Hello", True, 10]
>>>x[2] == >>>y[2]

```
### Accessing elements in a python list
1. The size of a list does not affect the average access time in the list
2. The average access time ay any location within a list is the same, regardless of its location in the list

We load XML data into turtle & display on a tkinter window

## Big-Oh Notation
Used as a way to measure the efficiency of our algorithms
* insert long, convoluted formula here*

#### Little-Oh Notation
* The same as Big-Oh, but upper bound cannot be equal to. < instead of <=

### Asymptotic analysis

f(x) ~ g(x) as x -> infinity

if the limit as x -> infinity of f(x) / g(x) approaches 1, we know both f(x) and g(x) approach the same value
### Runtimes (the good stuff :))
1. O(1) - constant
2. O(n) - linear
3. O(logn) - log
4. O(nlogn) - n * logn
4. O(n^c) - i.e. n^2, n^3, .... n^ c
5. O(2^n) - could also have different bases (3 ^ c)
    
