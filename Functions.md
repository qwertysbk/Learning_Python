# Python Functions
A function is a block of code which only runs when it is called.
You can pass data, known as parameters, into a function.  
A function can return data as a result.

### Creating a Function
In Python a function is defined using the `def` keyword.

### Calling a Function
To call a function, use the function name followed by parenthesis - `function_name()`.

```python
#Example
def my_function():
  print("Hello from a function")

my_function()
#Output : Hello from a function
```

### Inner functions
Inner functions can be useful in situations where you need to define a helper function that is only used inside another function,  
and you don't want to clutter the global namespace with unnecessary function names.
```py
def outer_func():
    def inner_func():
        print("This is an inner function.") 
    print("This is the outer function.")
    inner_func()

outer_func()
""" Output :
This is the outer function.
This is an inner function.
"""
```

### Recursion
Python also accepts function recursion, which means a defined function can call itself.
```py
def recc(x):
  if(x > 0):
    result = recc(x - 1)+x
    print(result)
  else:
    result = 0
  return result
print("\n\nRecursion Example Results")
recc(5)
"""
Output : 
Recursion Example Results
1
3
6
10
15
"""
```

### Empty Function
Function definitions cannot be empty, but if you for some reason have a function definition with no content,  
put in the pass statement to avoid getting an error.
```py
# Example
def myfunction():
  pass

# having an empty function definition like this, would raise an error without the pass statement
```

### Arguments
- Information can be passed into functions as arguments.  
- Arguments are specified after the function name, inside the parentheses`( )`.  
- You can add as many arguments as you want, just separate them with a comma.  
```python
#The following example has a function with one argument(fname)
def name(fname):
  print("Hello "+fname)

name("Bharath")
name("Amber")
#Output : Hello Bharath
#Output : Hello Amber
```
- Arguments are often shortened to 'args' in Python documentations.  
- The terms 'parameter' and 'argument' can be used for the information that are passed into a function.  
- From a function's perspective:  
-- A parameter is the variable listed inside the parentheses in the function definition.  
-- An argument is the value that is sent to the function when it is called.

### Number of Arguments
- By default, a function must be called with the correct number of arguments.  
- Meaning that if your function expects 2 arguments, you have to call the function with 2 arguments, not more, and not less.
```python
#Example 
def my_function(fname, lname):
  print(fname + " " + lname)

my_function("Harry", "Styles")
#Output : Harry Styles
```
### Arbitrary Arguments, *args
If you do not know how many arguments that will be passed into your function,  
add a * before the parameter name in the function definition.
```py
#Example
#If the number of arguments is unknown, add a * before the parameter name:

def my_function(*laptops):
  print("My Laptop is " + laptops[2])

my_function("Mac", "HP", "Dell")
#Output : My Laptop is Dell
```
###  Keyword Arguments
You can also send arguments with the key = value syntax.
```py
#Example
def my_function(a, b, c):
  print("My name is " + c)

my_function(a = "Ram", b = "Krishna", c = "Bharath")
#Output : My name is Bharath
```
### Default Parameter Value
If we call the function without argument, it uses the default value.
```py
#Example
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("India")
my_function()
my_function("Brazil")
"""
Output : I am from India
I am from Norway
I am from Brazil
"""
```
### Return Values
To let a function return a value, use the return statement:
```py
#Example
def my_function(x):
  return 5 * x

print(my_function(3))
print(my_function(5))
print(my_function(9))
"""
Output :
15
25
45
"""
```

### Local and Global Variables
In Python, a variable can have a global or local scope depending on where it is defined.

A `global variable` is a variable that is defined outside of any function and can be accessed from anywhere in the code,  
including inside functions. To define a global variable, simply assign a value to a variable outside of any function:

```python
my_var = 42  # this is a global variable
```
A `local variable` is a variable that is defined inside a function and can only be accessed from within that function.  
To define a local variable, simply assign a value to a variable inside a function:

```python
def my_func():
    my_var = 42  # this is a local variable
```
If a variable with the same name is defined both globally and locally,  
the local variable takes precedence inside the function.
```py
#Example:
my_var = 1  # this is a global variable

def my_func():
    my_var = 2  # this is a local variable
    print("Inside the function, my_var is", my_var)

my_func()
print("Outside the function, my_var is", my_var)
"""
Output of calling my_func would be:
Inside the function, my_var is 2

Output of printing my_var outside the function would be:
Outside the function, my_var is 1
"""
```
To access a global variable from inside a function,you can use the `global` keyword to indicate  
that you want to refer to the global variable rather than a local variable with the same name.
```py
#Example:
my_var = 1  # this is a global variable
def my_func():
    global my_var
    my_var = 2  # this modifies the global variable
    print("Inside the function, my_var is", my_var)

my_func()
print("Outside the function, my_var is", my_var)

"""
Output :
The output of calling my_func would be:
Inside the function, my_var is 2

The output of printing my_var outside the function would be:
Outside the function, my_var is 2
"""
```

### Examples 
```py
#Add 2 numbers using functions
def add_numbers(a, b):
    return(a + b)

print(add_numbers(4,9))
#Output : 13
#or
def add_numbers(a, b):
    return(a + b)
    
result = add_numbers(5, 10)
print(result)
#Output : 15
```
```py
#Factorial of given number
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)
        
print(factorial(5))
#Output : 120
```
