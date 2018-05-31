# Hashtables cont, Trees

## Hashmap
* Python's built in dictionary. Set is a collection of unique items

``` python
d = dict()
d.add('entry', -20)
OR
d['entry'] = -20


```
Complexities:
1. add -- O(1)
2. remove -- O(1)


``` python

import hashset
class HashMap:
    class __kyPair:
    def __init__(self, key, value):
        self.key = key
        self.value = value
    
    def __eq__(self, other):
        if type(self) != type(other):
            return False
        return self.value == other.value
        
    def __hash__(self):
        return hash(self.key)
        
    def __contains__(self, item):
        return HashMap.__keyPair(item, None) in self.hset
        
    def __setItem__(self, key, value):
        self.hset.add(HashMap__kypair(key, value))
        
```

## Add page 2
