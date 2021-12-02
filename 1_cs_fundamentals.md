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

## Useful built-in functions
**sorted**
```python
sorted(input, key=func)

# for example:
sorted([1,6,2]) # returns [1,2,6], using default sorting method
sorted(myList, key=len) # returns myList sorted by length
```
**len**
```python
len(input) # returns the number of elements in a list, characters in a string, keys in a dictionary, etc

# for example:
len([1,9,7]) # 3
len("asdf") # 4
len({'a': 'A', 'b': 2}) #2
```

**type**
```python
type(3) # int
type("asdf") # string
type([1,2,3]) # list
```
## Comparators
Compare by identity: `objA is objB`

Compare by value: `objA == objB`

Example:
```python
numbers = [1, 2, 3]
numbers2 = [1, 2, 3]
print(numbers == numbers2) # True
print(numbers is numbers2) # False
```

## Lists
Last element of a list:
```python
myList[-1] # this is the preferred "Pythonic" syntax
myList[len(myList) -1] # also works, but not as much of a tasty syntax snaq
```

You can also get the nth last element of a list with `myList[-n]`, for example the 3rd last element is `myList[-3]`. Nice!

## String manipulation (often helpful for algorithm problems)

Useful buiilt-in string methods: 
* isalpha()
* isnumeric()
* swapcase()
* isupper(), islower()
* upper(), lower()
* count("x") # how many times does "x" appear in the string

#### Joining strings:
```python
''.join(stringList)
```
This concatenates everything together with the string before the `.join` as a spacer. For example:
```python
stringList = ('My', 'name', 'is', 'Josh') # Same behavior with an array or other iterable
print(''.join(stringList)) # MynameisJosh
print(' '.join(stringList)) # My name is Josh
print('!!!'.join(stringList)) # My!!!name!!!is!!!Josh
```

#### Splitting strings:
Use the helpful `split` method from the string class:
```python
text.split() # splits at each space in a string. Helpful for turning a sentence into a word list
text.split(',') # split at each commma (or any custom string you pass in as the delimiter)
```

#### Reverse a string or array: 
```python
reverse = original[::-1]
```

#### Find and replace within a string:
```python
replace(' ', '_') # replace all linstances of the first argument with the second. (Spaces to underscores in this example)
```

## Fabulous for loops
for loop with index:
```python
for (i, item) in enumerate(items):
  # do stuff for each item, with index i
```

Iterate over a range:
```python
for i in range(n): #iterate from i = 0 to i = n-1
  print(i)
```

Python ranges are set up to not include the upper value, as this is most helpful considering that lists and other data structures are indexed from 0. A range can also be defined with a start value, for example `range(3,7)` includes 3, 4, 5, and 6.

## Getting fancy: list comprehensions
Often in algorithms problems you'll want to modify a list, and Python provides a very beautiful way to do so. This is language-specific so don't put too much energy into becoming an expert at this syntax -- you can always just use a for loop instead. But for some this more readable syntax is irresistible!

For example:
```python
nums = [1,2,3,4,5]

# The long way
squared = []
for n in nums:
  squared.append(n*n)

# The clever one-liner way, using list comprehension
squared = [x*x for x in nums]
```

You can also include conditional logic. In general, it works like this:
```python
new_list = [expression for member in iterable if conditional]
```

## Mutability and Functions 
Note that in Python, mutable types **can be modified** by functions that receive them as arguments! This is a key difference from other languages like JavaScript, where function arguments are always passed by value and the variable within the function is essentially a copy rather than the original value. Just be safe and avoid mutating the original arguments in your programs. For example:
```python
def safeSort(inputList):
  sortedList = list(inputList) # inputList.copy() works too
  sortedList.sort() # the sort method, like many other built-in methods you'll use, mutates the list
  return sortedList

# Don't do this! :x
def livingDangerously(inputList):
  inputList.sort() # mutates the original, outside of the function scope
  return inputList
```

Note how we define a new list using a list constructor or by copying the other list, rather than using equals assign. Just like in JavaScript, `sortedList = inputList` creates a new pointer (reference) to the same object in memory rather than creating a new object. While Python keeps things a lot more logical and predicatable than JavaScript when it comes to mutations, this "pass by reference" behavior in functions is one big execption that you need to look out for. 

For new Python devs, this means remembering that any changes you make to arguments within a function will also apply outside the function. Better yet, simply avoid this possibility altogether by using non-mutating built-in methods like `sorted` rather than mutating class methods.

## Learn to love the Python docs! Start here:
* Built-in types: https://docs.python.org/3/library/stdtypes.html
* Built-in functions: https://docs.python.org/3/library/functions.html
* String constants: https://docs.python.org/3.9/library/string.html
* List comprehensions: https://docs.python.org/3/tutorial/datastructures.html#list-comprehensions

## Lecture Slides
* [Python I](https://docs.google.com/presentation/d/1YwuicgzQFipK7Uymlq5Fm6Aq_PTPPm-4s6-XaXyp5T8/edit?usp=sharing)
* [Python II](https://docs.google.com/presentation/d/1W5pYcqYYgfhyYnISbIrLu__6HFcUJTqyDHirYPtMd24/edit?usp=sharing)
* [Python III](https://docs.google.com/presentation/d/1ZvCbSK-uFqrpyYMPrudCayV6thTzqLfwT-eIudC_fnY/edit?usp=sharing)
* [Python IV](https://docs.google.com/presentation/d/17g5vepthZ-R582Z9CBJwzH2TMJHDMI6LTxy6e7wrp2o/edit?usp=sharing)

## More resources:
* [The ultimate guide for data structures & algorithm interviews](https://dev.to/rahhularora/the-ultimate-guide-for-data-structures-algorithm-interviews-npo)
