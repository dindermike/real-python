# String Formatting (f-strings)
---
In Python String Formatting, commonly known as f-strings is a minimalistic and convenient way to embed expressions inside string literals, using curly braces `{}`. Introduced in Python 3.6, f-strings provide a more readable and concise syntax for formatting strings compared to older methods like `str.format()` or the `%` operator. It was introduced in order to satisfy the PEP8 Style Guide PEP-498 Rule (Literal String Interpolation), which evaluates an expression at run-time and is not a constant value.

## Basic Usage
To create an f-string, prefix the string with the letter `f`. Inside the string, you can include variables within curly braces `{}` that will be evaluated at runtime.
```python
name = 'Mike'
age = 39
greeting = f'Hello, my name is {name} and I am {age} years old.'
print(greeting)
```
**Output:** <mark>Hello, my name is Mike and I am 39 years old.</mark>

## Conditional Expressions
You can include conditional expressions within f-strings to dynamically change the output based on certain conditions. For example, show the word `Passed` if the value of `score` is greater than or equal to `60`, else show the word `Failed`:
```python
score = 85
result = f'You have {"Passed" if score >= 60 else "Failed"} the exam!'
print(result)
```
**Output:** <mark>You have Passed the exam!</mark>

## Method Invocations
You can call methods directly within the curly braces of an f-string. For example, to format a name with title case:
```python
name = 'bilbo baggins'
greeting = f'Hello, {name.title()}!'
print(greeting)
```
**Output:** <mark>Hello, Bilbo Baggins!</mark>

## Format Specifiers
You can use format specifiers to control the formatting of numbers, dates, and other types. For example, to format a floating-point number, rounded to two decimal places:[^1]
```python
import math
e = math.e
formatted_e = f"Euler's Number rounded to 2 decimal places: {e:.2f}"
print(e)
print(formatted_e)
``` 
**Output:** <mark>2.718281828459045</mark><br />
&emsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;<mark>Euler's Number rounded to 2 decimal places: 2.72</mark>

*Here, we are using the double quote rather than the single quote to demonstrate that f-strings can be created with either type of quotation marks and is done so here to avoid confusion with the apostrophe in "Euler's".*

[^1]: Note: The format specifier `:.2f` indicates that the number should be formatted as a floating-point number with 2 digits after the decimal point. This will round the number following "Bankers' Rounding" rules. To round up or down consistently, consider using the `math.ceil()` or the `math.floor()` methods instead.

## Multiline f-strings
F-strings can also span multiple lines using triple quotes. This is useful for creating longer strings that require formatting.
```python
name = 'Frodo Baggins'
age = 50
occupation = 'ring bearer'
bio = f'''Name: {name}
Age: {age}
Occupation: {occupation.title()}'''
print(bio)
```
**Output:** <mark>Name: Frodo Baggins</mark><br />
&emsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;<mark>Age: 50</mark><br />
&emsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;<mark>Occupation: Ring Bearer</mark>

## To Recap
F-strings provide a powerful and flexible way to format strings in Python. They allow for embedding expressions, conditional logic, method calls, and formatting specifications directly within string literals, making code more readable and concise.