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

### Passing by value vs reference
Note that in Python, mutable types **can be modified** by functions that receive them as arguments! This is a key difference from other languages like JavaScript, where function arguments are always passed by value and the variable within the function is essentially a copy rather than the original value. Just be safe and avoid mutating the original arguments in your programs. For example:
```
def safeSort(inputList):
  sortedList = list(inputList) # inputList.copy() works too
  sortedList.sort() # the sort method, like many other built-in methods you'll use, mutates the list
  return sortedList

# Don't do this! :x
def livingDangerously(inputList):
  inputList.sort() # mutates the original, outside of the function scope
  return inputList
```

Note how we define a new list using a list constructor or by copying the other list, rather than using equals assign. Just like in JavaScript, `sortedList = inputList` creates a new pointer (reference) to the same object in memory rather than creating a new object. While Python keeps things a lot more logical and predicatable than JavaScript when it comes to mutations, this "pass by reference" behavior in functions is one big execption that you need to look out for. For new Python devs, this means always remembering that any changes you make to arguments within a function will also apply outside the function.

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
stringList = ('My', 'name', 'is', 'Josh') # Same behavior with an array or other iterable
print(''.join(stringList)) # MynameisJosh
print(' '.join(stringList)) # My name is Josh
print('!!!'.join(stringList)) # My!!!name!!!is!!!Josh
```

#### Reverse a string or array: 
```
reverse = original[::-1]
```


## Learn to love the Python docs! Start here:
* Built in types: https://docs.python.org/3/library/stdtypes.html
* String constants: https://docs.python.org/3.9/library/string.html

## Lecture Slides
* [Python I](https://docs.google.com/presentation/d/1YwuicgzQFipK7Uymlq5Fm6Aq_PTPPm-4s6-XaXyp5T8/edit?usp=sharing)
* [Python II](https://docs.google.com/presentation/d/1W5pYcqYYgfhyYnISbIrLu__6HFcUJTqyDHirYPtMd24/edit?usp=sharing)
* Python III
* Python IV

## More resources:
* [The ultimate guide for data structures & algorithm interviews](https://dev.to/rahhularora/the-ultimate-guide-for-data-structures-algorithm-interviews-npo)
