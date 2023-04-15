## Conditional Statements in Python

Conditional statements in Python allow you to control the flow of your program based on certain conditions.
These statements are used to execute certain statements only if a particular condition is satisfied.

### If Statement

The `if` statement is used to check whether a condition is true or false.
If the condition is true, then the code inside the if block will be executed.
```python
x = 5
if x > 0:
    print("x is a positive number")
    
#Output : x is a positive number
```

### if-else Statement
The `if-else` statement is used when you want to execute one block of code if the condition is true
and another block of code if the condition is false.
```python
if condition:
    # code to be executed if condition is True
else:
    # code to be executed if condition is False
```
#### For example:

```python
x = -5
if x > 0:
    print("x is a positive number")
else:
    print("x is a negative number")
    
#Output: x is a negative number
```

### If-elif-else Statement
The `if-elif-else` statement is used when you have multiple conditions to check.
The `elif` keyword is used to add additional conditions to check,
and the `else` block is executed if none of the conditions are true.
```python
if condition1:
    # code to be executed if condition1 is True
elif condition2:
    # code to be executed if condition2 is True
else:
    # code to be executed if none of the conditions are True
```
#### For example:

```python
x = 0
if x > 0:
    print("x is a positive number")
elif x == 0:
    print("x is zero")
else:
    print("x is a negative number")

#Output: x is zero
```

### Nested If Statements
`Nested if` statements are used when you have to check for multiple conditions inside a single if block.
```python
if condition1:
    # code to be executed if condition1 is True
    if condition2:
        # code to be executed if condition2 is True
```
#### For example:

```python
x = 10
if x > 0:
    print("x is a positive number")
    if x > 10:
        print("x is greater than 10")
    elif x == 10:
        print("x is equal to 10")
    else:
        print("x is less than 10")
else:
    print("x is a negative number")

#Output: 
#x is a positive number
#x is greater than 10
```

## Looping Statements in Python
Looping statements are a fundamental feature of programming that allow you to execute a block of code multiple times.
Python provides two main types of looping statements: for loops and while loops.

### for Loops
The `for loop` in Python is used to iterate over a sequence (e.g., a list, tuple, or string)
and execute a block of code for each item in the sequence.

```python
# Syntax of a for loop
for item in sequence:
    # code block to be executed for each item in the sequence
```
#### For example :
```python
# Example of a for loop
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)
"""
Output:
1
2
3
4
5
"""

#You can also use the range() function with a for loop to iterate a specific number of times:

# Example of a for loop using range
for i in range(5):
    print(i)

"""
Output:
0
1
2
3
4
"""
```
### while Loops
The `while loop` in Python is used to execute a block of code repeatedly as long as a condition is true.

```python
# Syntax of a while loop
while condition:
    # code block to be executed as long as the condition is true
```
#### For example :
```python
# Example of a while loop
count = 1
while count <= 5:
    print(count)
    count += 1

"""
Output:
1
2
3
4
5
"""
Note : it's important to make sure the condition in a while loop eventually becomes False to avoid an infinite loop.
```

### break and continue Statements
Python also provides two special statements that can be used inside loops:
#### break
The `break` statement is used to exit a loop prematurely:
```python
# Example of a break statement in a for loop
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    if num == 3:
        break
    print(num)
    
"""
Output:
1
2
"""
```
#### continue
The `continue` statement is used to skip the rest of the current iteration and move on to the next one:
```python
# Example of a continue statement in a while loop
count = 0
while count < 5:
    count += 1
    if count == 3:
        continue
    print(count)
    
"""
Output:
1
2
4
5
"""
```
This concludes the documentation of Looping and Conditional statements in Python
