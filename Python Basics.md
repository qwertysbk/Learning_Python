# Python Basics

## Variable Types and Examples

This document describes different variable types in Python and provides examples of each.

### Integer Variable
An integer variable stores whole numbers, positive or negative, without decimals. Examples:
```python
x = 5
```

### Float Variable
A float variable stores floating-point numbers, which are numbers with a decimal point. Examples:
```python
y = 2.5
```

### String Variable
A string variable stores a sequence of characters, such as letters, numbers, and symbols. Examples:
```python
name = "John"
```

### List Variable
A list variable stores a collection of items, which can be of different types. Lists are ordered and mutable, meaning their elements can be changed. Examples:
```python
my_list = [1, 2, 3, 4, 5]
```

### Tuple Variable
A tuple variable stores a collection of items, which can be of different types. Tuples are ordered and immutable, meaning their elements cannot be changed. Examples:
```python
my_tuple = (1, 2, 3, 4, 5)
```

### Dictionary Variable
A dictionary variable stores a collection of key-value pairs, where each key is associated with a value. Dictionaries are unordered and mutable. Examples:
```python
my_dict = {"name": "John", "age": 30}
```

This concludes the documentation for different variable types in Python.


## Built-in Data Types in Python

Python provides several built-in data types that can be used to represent different kinds of values. The most common data types in Python include:

### Numeric Types

Python has three built-in numeric data types:

- `int`: Used to represent integers (whole numbers) such as `-10`, `0`, or `100`.
```python
x = 10
print(type(x))  # Output: <class 'int'>
```

- `float`: Used to represent floating-point numbers (decimal numbers) such as `3.14`, `0.5`, or `-2.0`.
```python
x = 3.14
print(type(x))  # Output: <class 'float'>
```

- `complex`: Used to represent complex numbers with real and imaginary parts such as `3 + 4j` or `-2.5 + 0.1j`.
```python
x = 3 + 4j
print(type(x))  # Output: <class 'complex'>
```

### Boolean Type
The Boolean data type is used to represent logical values that can either be `True` or `False`.
```python
x = True
print(type(x))  # Output: <class 'bool'>
```

### Sequence Types
Python has several built-in sequence types:

- `list`: Used to represent ordered collections of values, which can be of any type. For example, `[1, 2, 3]` or `["apple", "banana", "cherry"]`.
```python
x = [1, 2, 3]
print(type(x))  # Output: <class 'list'>
```

- `tuple`: Similar to lists, but they are immutable (cannot be changed). For example, `(1, 2, 3)` or `("apple", "banana", "cherry")`.
```python
x = (1, 2, 3)
print(type(x))  # Output: <class 'tuple'>
```

- `range`: Used to represent a sequence of numbers. For example, `range(0, 10)` represents the numbers `0` through `9`.
```python
x = range(0, 10)
print(type(x))  # Output: <class 'range'>
```

### Set Types
Python has two built-in set types:

- `set`: Used to represent an unordered collection of unique elements. For example, `{1, 2, 3}`.
```python
x = {1, 2, 3}
print(type(x))  # Output: <class 'set'>
```

- `frozenset`: Similar to sets, but they are immutable (cannot be changed). For example, `frozenset({1, 2, 3})`.
```python
# Example of frozenset data type
x = frozenset({1, 2, 3})
print(type(x))  # Output: <class 'frozenset'>
```

This concludes the documentation for different built in data types in Python.


## Type Conversions in Python

In Python, type conversion refers to the process of changing the data type of a variable from one data type to another. This is also known as type casting.

Python supports several built-in functions for type conversion. These functions can be used to convert variables from one data type to another.

### 1. Integer Conversion

To convert a variable to an integer data type, you can use the `int()` function. This function takes a single argument and returns an integer value. If the argument is a string, it must contain a valid integer value, otherwise a `ValueError` will be raised.
```python
x = 5.6
y = "10"
z = int(x) # z will be 5
w = int(y) # w will be 10
```

### 2. Float Conversion
To convert a variable to a float data type, you can use the `float()` function. This function takes a single argument
If the argument is a string, it must contain a valid floating-point value, otherwise a `ValueError` will be raised.
```python
x = 5
y = "3.14"
z = float(x) # z will be 5.0
w = float(y) # w will be 3.14
```

### 3. String Conversion
To convert a variable to a string data type, you can use the `str()` function. This function takes a single argument and returns a string representation of the argument.
```python
x = 5
y = 3.14
z = str(x) # z will be "5"
w = str(y) # w will be "3.14"
```

### 4. Boolean Conversion
To convert a variable to a boolean data type, you can use the `bool()` function. This function takes a single argument and returns a boolean value. Any non-zero value will be converted to `True`, while `0` and `None` will be converted to `False`.
```python
x = 5
y = 0
z = bool(x) # z will be True
w = bool(y) # w will be False
```

This concludes the documentation for different built in data types in Python.


## Inputs and Outputs in Python

In Python, you can read inputs from the user and display outputs to the user. This can be done using the `input()` and `print()` functions respectively.

### Reading Inputs
To read input from the user, you can use the `input()` function. This function takes a single argument, which is a prompt message to display to the user. The user can then enter a value, which will be returned by the function as a string.
```python
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

### Displaying Outputs
To use the `print()` function. This function takes one or more arguments, which are the values to be displayed. The values are separated by commas, and by default, are separated by a space.
```python
x = 5
y = 10
print("The sum of", x, "and", y, "is", x + y)
```

### Formatted Output
You can use formatted output to display values in a specific format. The `format()` function can be used to format values and insert them into a string.
```python
name = "John"
age = 25
print("My name is {} and I am {} years old.".format(name, age))
```
You can also use f-strings to achieve the same result in a more concise way:
```python
name = "John"
age = 25
print(f"My name is {name} and I am {age} years old.")
```

This concludes the documentation for Inputs and Outputs in Python


## Built-in Functions in Python

Python comes with a number of built-in functions that are used frequently when writing code. These functions are always available in your Python environment, so you don't need to import any libraries to use them. In this report, we'll cover a few of the most commonly used built-in functions in Python.

### print()
The `print()` function is used to display output to the console. You can pass one or more arguments to the function, and they will be displayed separated by spaces.
```python
print("Hello, world!")
print("The answer is", 42)
#Output :
#Hello, world!
#The answer is 42
```

### input()
The `input()` function is used to read input from the user. When called, the function will display a message to the user, and then wait for the user to enter a value. The value entered by the user is returned as a string.
```python
name = input("What is your name? ")
print("Hello,", name)
#Output :
#What is your name? Alice
#Hello, Alice
```

### len()
The `len` function is used to get the length of a sequence, such as a string, list, or tuple.
```python
name = "Alice"
print(len(name))
#Output : 5

numbers = [1, 2, 3, 4, 5]
print(len(numbers))
#Output : 5
```

### str(), int(), and float()
The `str()`, `int()`, and `float()` functions are used to convert values from one data type to another.
```python
number_str = "42"
number_int = int(number_str)
print(number_int)   # Output: 42

price_str = "3.14"
price_float = float(price_str)
print(price_float)  # Output: 3.14

name = "Alice"
name_str = str(name)
print(name_str)     # Output: "Alice"
```

### range()
The `range()` function is used to create a sequence of numbers. It takes one, two, or three arguments, depending on how you want to use it.
```python
for i in range(10):
    print(i)
#Output :
"""
0
1
2
3
4
5
6
7
8
9
"""


for i in range(2, 10):
    print(i)
#Output :
"""
2
3
4
5
6
7
8
9
"""

for i in range(1, 10, 2):
    print(i)
#Output :
"""
1
3
5
7
9
"""
```

### max() and min()
The `max()` and `min()` functions are used to find the largest and smallest values in a sequence, respectively.
```python
numbers = [3, 7, 1, 9, 4, 2]
largest = max(numbers)
smallest = min(numbers)
print("The largest number is:", largest)
print("The smallest number is:", smallest)
#Output :
#The largest number is: 9
#The smallest number is: 1
```

This concludes the documentation for some built-in functions in Python
