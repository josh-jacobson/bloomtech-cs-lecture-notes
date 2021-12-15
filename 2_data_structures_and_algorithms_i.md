# Sprint 2: Data Structures and Algorithms

## Helpful Python operators
Modulus: %
```python
print(5 % 2) # 1
```
Floor division: //
```python
print(5 // 2) # 2
```

String to ASCII code: `ord`
```python

ascii_code = ord("J")
print(ascii_code) # 74
```
ASCII code to string: `chr`
```python
my_string = chr(74)
print(my_string) # "J"
```

## Number bases
One way to think of the "base" of a number system is how many digits we have to work with.

In base ten, popular among humans these days, we have 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9. Ten digits total!

In base two (binary): just have two possible digits: 0 and 1.

Another way to think about this is when we're counting, at what point do we "carry over" and add a second digit? 

We can count 1, 2, 3, ... all the way up to 9 but then what's that next value, the one represented by all of our fingers? We "start over" at 0 and add a 1 out front to get "10". That carry-over point where we have to add another digit to represent the value is 10 for base 10, 2 for base 2, 16 for hexadecimal, etc.

## Binary and Hex

Because coumputers are built around transistors with on/off, 0/1 binary behavior, all computer operations are actually dealing with binary values. Base 10 doesn't really make sense for computers because it's not a power of 2! You'll often see hexadecimal numbers as a more readable, compact representation of a binary number. Four binary digits can be represented by a single hexadecimal digit. Let's see how:

In base 16 (Hexadecimal), we have 16 different possible digits. Imagine that you had sixteen fingers instead of ten, and we had five additional words used for counting verbally. For the sake of simplicity, we represent hexadecimal numbers using the digits we know (0-9) plus the first five letters of the alphabet. A is ten, B is eleven, and so on:
* 0xA = 10 = 0b1010
* 0xB = 11 = 0b1011
* 0xC = 12 = 0b1100
* 0xD = 13 = 0b1101
* 0xE = 14 = 0b1110
* 0xF = 15 = 0b1111

Basic data types and memory addresses are generally stored as 32-bit or 64-bit values. Rather than writing out those very long values, we can use hexadecimal notation:
| Hexadecimal | Binary |
|---|---|
| 0xabc1 (4 hex digits) | 10101011 11000001 (16 bits) |
| 0xf9ab1234 (8 hex digits) | 011111001 10101011 00010010 00110100 (32 bits) |

As you can see, every hexadecimal digit represents 4 binary digits. This makes sense because 16 = 2^4.


## Converting between bases in Python
The following are all equivalent ways to assign an integer to a variable in Python:
```python
a = 0b1001010 # binary representation of 74
b = 0x4a # hexadecimal representaion of 74
c = 74
print(a == b) # True
print(b == c) # True
```
The default print formatting uses the base 10 representation that feels "normal" to us humans. Sometimes for algorithms problems, however, you'd like to work with a binary or hexadecimal representation directly. Use these methods to return those representations **as a string**: 
```python
>>> a = bin(88)
>>> print(a)
'0b1011000' # the '0b' out front indicates binary
>>> type(a)
<class 'str'>

>>> hex(88)
'0x58' # the '0x' out front indicates hexadecimal
```

Likewise, to convert back from a string representation to an int:
```python
>>> int('0b1011000', 2) # specify the base (2 for binary) as the second argument
88
>>> int('0x58', 16) # convert from hexadecimal representation (base 16)
88
```

## String Encoding
ASCII stands for American Standard Code for Information Interchange, and is a simple mapping of numbers to printable characters. The full table is linked below for reference, here are a few examples:
| Character | ASCII code (decimal) | Binary | Hexadecimal |
|---|---|---|---|
| A | 65 | 0b01000001 | 0x41 |
| a | 97 | 0b01100001 | 0x61 |
| J | 74 | 0b01001010 | 0x4A |
| / | 47 | 0b00101111 | 0x2F |

Note how "A" and "a" in binary representation both look like "1" with a different header out front. Clever! In ASCII, the codes for any letter and its lowercase version are always 32 apart, equivalent to flipping the 5th bit in binary.

ASCII dates back to to 1963 and was designed with telegraph systems in mind, using a meager 7 bits to provide 128 (2^7) possible characters. 33 of these were reserved for control characters like "carriage return" and "end of transmission", so there really weren't that many character options. In 1981 IBM developed "Extended ASCII" for personal computers, adding the 8th bit for a whopping 256 characters! Still very limiting, and different variations had to be developed for different languages so nothing was standardized in the way we require for reliable international communications. Maybe <256 characters is okay for the basic Latin alphabet used by English and other Romance languages, but what about more complex languages like Chinese, Korean, Japanese...and symbols and emojis!? 🧘‍♀️🔮💾 

Enter Unicode, a universal character set with the intention to include all characters needed for all human languages. This is a more complex approach with variable 8, 16, or up to 32-bit encoding. With this system we could have up to 1,111,998 possible characters! You can think of Unicode as a superset of the ASCII character set since the first 128 characters are the same. UTF-8, also known as HTML Unicode, is the most common encoding system for Unicode and is used for almost all (97.6%) web pages.

Specifics aside, the key thing to remember is that **string characters are represented in computer memory just like integers, and we use a simple lookup table to create a mapping from number to char.**


## Lecture slides
* [Number Bases and Character Encoding](https://docs.google.com/presentation/d/17g5vepthZ-R582Z9CBJwzH2TMJHDMI6LTxy6e7wrp2o/edit?usp=sharing)
* [Hash Tables I]()
* [Hash Tables II]()
* [Searching and Recursion]()

## Helpful resources
* [Math is Fun - Number Bases](https://www.mathsisfun.com/numbers/bases.html)
* [ASCII Table](https://www.ascii-code.com/)
* [Characters, Symbols and the Unicode Miracle - Computerphile](https://www.youtube.com/watch?v=MijmeoH9LT4&ab_channel=Computerphile)
