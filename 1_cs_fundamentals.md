# Sprint 1: Computer Science Fundamentals

## Python Data Types
### Immutable data types (pass by value)
* int
* float
* bool
* str
* unicode
* tuple

### Mutable data types (pass by reference)
* List
* Dictionary
* Set
* Array

Iterables: List, Tuple, String, Dictionary and Set.
(Also any objects you define with an __iter__() or __getitem()__ method)

## Comparators
Compare by identity: `objA is objB`

Compare by value: `objA == objB`

Example:
```
numbers = [1, 2, 3]
numbers2 = [1, 2, 3]
print(numbers == numbers2) # True
print(numbers is numbers2) # False
```

## String manipulation (helpful for CodeSignal algorithm challenges!)

Useful buiilt-in string methods: 
* isalpha()
* isnumeric()
* swapcase()

#### Joining strings:
```
''.join(stringList)
```
This concatenates everything together with the string before the `.join` as a spacer. For example:
```
stringList = ('My', 'name', 'is', 'Josh')
print(''.join(stringList)) # MynameisJosh
print(' '.join(stringList)) # My name is Josh
print('!!!'.join(stringList)) # My!!!name!!!is!!!Josh

```
This works with arrays and other iterables too.


#### Reverse a string or array: 
```
reverse = original[::-1]
```


### More resources
* Built in types: https://docs.python.org/3/library/stdtypes.html
* String constants: https://docs.python.org/3.9/library/string.html
