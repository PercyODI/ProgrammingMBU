# Python Script for Teachers

https://automatetheboringstuff.com/chapter1/

## Getting started in the Python Shell

Open the Python IDLE

`Start -> Type Python -> Click IDLE (Python 3.7 64-bit)`
- Note: Make sure you and the students open Python 3.x. NO 2.7!!

When the program opens, it should say at the top what version of Python you are running. Then 3 arrows `>>>`. Those 3 arrows are telling us that the shell is waiting on us to tell it to do something.

## Math and Expressions

Computers are good at math! Python could easily be used as a calculator for us.

Let's try something easy. Just 2 + 2. Make sure you click into the window and have a flashing cursor after the 3 arrows. We are just going to type 2 + 2.

`>>> 2 + 2`

Now click enter. The shell should have responded with the answer (4), and then presented us with 3 arrows again.

What we gave the shell is called an ***Expression***. Expressions are just ***Values*** (like the number 2) and ***Operators*** (like the plus sign). When given an expression, Python is ***Evaluate*** it down to a single value (in this case 4).

> Is a value by itself an expression? What happens if you just type a single number with no operator?

As you have seen, a value by itself is still evaluated by Python down to a single value. It is technically an expression!

> What other operators can we try?

Operator | Definition | Example
--|--|--
+ | Addition | 2 + 2 = 4
- | Subtraction | 5 - 2 = 3
* | Multiplication | 3 * 5 = 15
/ | Division | 22 / 8 = 2.75
** | Exponent | 2 ** 3 = 8
// | Integer division | 22 / 8 = 2
% | Modulus / Remainder | 22 % 8 = 6

Order of Operations matters. Do you remember PEMDAS?
Parentheses -> Exponents -> Multiplication/Division -> Addition/Subtraction.

This order matters to Python as well. Let's take a look

```python
>>> 2 + 3 * 6
20
>>> (2 + 3) * 6
30
>>> (5 - 1) * ((7 + 1) / (3 - 1))
16.0
```

> What happens if we type a bad expression? How does Python handle it?

```python
>>> 5 + 
SyntaxError: invalid syntax

>>> 42 + 5 + * 2
SyntaxError: invalid syntax
```

Oh no! Errors! Don't freak out about errors! The interpreter is just trying to help you find out what you have messed up.

Don't worry about breaking the computer. Error are normal and common. Professionals deal with them all the time.

## Number Types
Computers think about numbers differently than we do. 
- Integers are whole numbers only. No decimals.
- Floating-point numbers have decimals.

You'll notice that any time you do an operation with at least one floating-point number, the result is always a floating-point number.

```python
>>> 4 * 2.3
9.2
>>> 5.4 + 2
7.4
>>> 8 / 2
4.0
```

Wait, why did `8 / 2` result in a floating point number? In Python 3, all division results in a floating point number, because even if dividing integers, you can still get a decimal answer.

## Strings
Ok, let's move away from numbers for a little bit. In Python, you can create a string type. A string is just text.

```python
>>> "Hello World!"
'Hello World!'
>>> "11 Cats"
'11 Cats'
```

>What happens if we try to add strings together?
```python
>>> "Alice" + "Bob"
'AliceBob'
```

> Is that what you expected would happen?

This is called String Concatenation. 

> What happens when we add a string and a number?
```python
>>> "Alice" + 42
Traceback (most recent call last):
File "<pyshell#10>", line 1, in <module>
"Alice" + 42
TypeError: can only concatenate str (not "int") to str
```

Python didn't like that.

> What does the TypeError tell us about what went wrong?

It can't concatenate an int and a str. We would have to convert the int into a str.

```python
>>> "Alice" + str(42)
'Alice42'
```

> What happens if we try to multiply a string by an integer? 

```python
>>> "Alice" * 5
'AliceAliceAliceAliceAlice'
```
