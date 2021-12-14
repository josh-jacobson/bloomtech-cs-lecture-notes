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

## Number bases
One way to think of the "base" of a number system is how many digits we have to work with.

In base ten, popular among humans these days, we have 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9. Ten digits total!

In base two (binary): just have two possible digits: 0 and 1.

Another way to think about this is when we're counting, at what point do we "carry over" and add a second digit? 

We can count 1, 2, 3, ... all the way up to 9 but then what's that next value, the one represented by all of our fingers? We "start over" at 0 and add a 1 out front to get "10". That carry-over point where we have to add another digit to represent the value is 10 for base 10, 2 for base 2, 16 for hexadecimal, etc.

## Binary and Hex

Because coumputers are built around transistors with on/off, 0/1 binary behavior, all computer operations are actually dealing with binary values. Base 10 doesn't really make sense for computers because it's not a power of 2! You'll often see hexadecimal numbers as a more readable, compact representation of a binary number. Four binary digits can be represented by a single hexadecimal digit. Let's see how:

An 8-digit binary number (aka 8 bits or 1 byte) can represent 256 (2^8) different values, inclusive from 0 to 255.
```
0b10000000 = 255
0b00001001 = 9
```

In base 16 (Hexadecimal), we have 16 different possible digits. These are represented with the digits we know (0-9) plus the first five letters of the alphabet:
* 0xA = 10 = 0b1010
* 0xB = 11 = 0b1011
* 0xC = 12 = 0b1100
* 0xD = 13 = 0b1101
* 0xE = 14 = 0b1110
* 0xF = 15 = 0b1111

Basic data types and memory addresses are generally stored as 32-bit or 64-bit values. Rather than writing out those very long values, we can use hexadecimal notation:
```
0xabc1 = 0b10101011 11000001 (16 bits)
0xf9ab1234 = 0b011111001 10101011 00010010 00110100 (32 bits)
```
As you can see, every hexadecimal digit represents 4 binary digits. This makes sense because 16 = 2^4.


## Converting between bases
Convert a "normal" int (base 10) to a binary representation:
```python
>>> bin(88)
'0b1011000' # the '0b' out front indicates binary
```

Binary to base 10:
```python
>>> int('0b1011000', 2) # specify the base (2 for binary) as the second argument
88
```

## String Encoding
ASCII stands for American Standard Code for Information Interchange, and is a simple mapping of 8-bit values to characters. The full table is linked below for reference, here are a few examples:
* 74 = 0b01001010 = 0x4A => "J"
* 47 = 0b00101111 = 0x2F => "/"

Originally ASCII was implemented with only 7 bits (128 possible characters), then the eighth bit was added on with variations of "Extended ASCII". Still a bit limiting, though. What about emojis!? 🧘‍♀️🔮💾 Enter Unicode, a more complex system with variable 8, 16, or 32-bit encoding. With this system we could have up to 1,111,998 possible characters! Much more options.

Specifics aside, the key thing to remember is that **string characters are represented in computer memory just like integers, and we use a simple lookup table to create a mapping from number to char.**

## Lecture slides
* [Number Bases and Character Encoding](https://docs.google.com/presentation/d/17g5vepthZ-R582Z9CBJwzH2TMJHDMI6LTxy6e7wrp2o/edit?usp=sharing)
* [Hash Tables I]()
* [Hash Tables II]()
* [Searching and Recursion]()

## Helpful resources
* [Math is Fun - Number Bases](https://www.mathsisfun.com/numbers/bases.html)
* [ASCII Table](https://www.ascii-code.com/)
