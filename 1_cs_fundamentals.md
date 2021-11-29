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

Useful string methods: isalpha(), isnumeric(), swapcase()

Joining list of strings:
```
''.join(stringList)
```
(Works with any iterable)

Reverse a string or array: 
```
reverse = original[::-1]
```

Iterables: Some of the example of iterables are:
Native data types - List, Tuple, String, Dictionary and Set.
File objects and objects you define with an __iter__() or __getitem()__ method.

### More resources
* Built in types: https://docs.python.org/3/library/stdtypes.html
* String constants: https://docs.python.org/3.9/library/string.html

