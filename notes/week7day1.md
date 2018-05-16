# Hashing, HashSet Class, Load-Factor, Separate Chaining, Open Addressing, Dictionaries, Intro to Trees

## **Common Final June 9th**

## Hashing
* Python has a built in set(). HashSet


``` python
x = set()
x.add(1)
x.add(2)
print(x)
(1, 2)

x.add(2)
print(x)

(1, 2)
#Cannot have copies of the same element
```
'insert' function has a positional parameter

### Abstract Data Type (ADT): Hashset
* Membership runs in O(1)
* Add runs in O(1)
* Remove runs in O(1)

#### Design Recipe
1. Description of the interface without the implementation
2. Probably gonna be on the common final

* Hash Function takes in an object, and returns the hashcode of an object. hash function does not yield completely unique numbers


``` python
class HashSet:
    def __init__(self, contents = []):
        self.items = [None] * 10
        self.numItems = 0
        
        for item in contents:
            self.add(item)
    

```

### Collision Resolution
* Open addressing
* Separate Chaining

``` python

def __add__(item, items):
    index = hash(item) % len(items)
    loc = -1 #flag for no placeholder found
    
    while items[index] != None:
        if items[index] == item:
            return False
            if loc < 0 and type(items[index]) == '\':
            HashSet.__PlaceHolder:
            loc = index
            
```



    
