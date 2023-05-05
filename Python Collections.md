# Python Collections (Arrays)
There are four collection data types in the Python programming language:  
- `List` is a collection which is ordered and changeable. Allows duplicate members.  
- `Tuple` is a collection which is ordered and unchangeable. Allows duplicate members.  
- `Set` is a collection which is unordered, unchangeable*, and unindexed. No duplicate members.  
- `Dictionary` is a collection which is ordered** and changeable. No duplicate members.  

## Python Lists

```py
mylist = ["apple", "banana", "cherry"]
```
Lists are used to store multiple items in a single variable.
Lists are created using square brackets`[]`:
- Create a List:
```py
l1 = ["apple", "banana", "cherry"]
print(l1)

#Output : ['apple', 'banana', 'cherry']
```
#### List Items

List items are ordered, changeable, and allow duplicate values.  
List items are indexed, the first item has index [0], the second item has index [1] etc.

#### Ordered

When we say that lists are ordered, it means that the items have a defined order, and that order will not change.  
If you add new items to a list, the new items will be placed at the end of the list.  

#### Changeable

The list is changeable, meaning that we can change, add, and remove items in a list after it has been created.

#### Allow Duplicates

Since lists are indexed, lists can have items with the same value:

```py
#Example 
l1 = ["apple", "banana", "cherry", "apple", "cherry"]
print(l1)

#Output : ['apple', 'banana', 'cherry', 'apple', 'cherry']
```
#### List Length
To determine how many items a list has, use the len() function:
```py
#Example - Print the number of items in the list
l1 = ["apple", "banana", "cherry"]
print(len(l1))

#Output : 3
```
#### List Items - Data Types
List items can be of any data type:
#### type()

From Python's perspective, lists are defined as objects with the data type : `<class 'list'>`
```py
#Example : String, int and boolean data types:
list1 = ["apple", "banana", "cherry"]
list2 = [1, 5, 7, 9, 3]
list3 = [True, False, False]
list4 = ["abc", 34, True, 40, "male"]
print((list4))
print(type(list4))

"""
Output :
['abc', 34, True, 40, 'male']
<class 'list'
"""
```
#### `list()` Constructor
It is also possible to use the `list()` constructor when creating a new list.
```py
#Example : Using the list() constructor to make a List:
l1 = list(("apple", "banana", "cherry")) # note the double round-brackets
print(l1)

#Output : ['apple', 'banana', 'cherry']
```
#### Access Items  
List items are indexed and you can access them by referring to the index number:
```
#Example :
list = ["apple", "banana", "cherry"]
print(list[0])
print(list[1])
print(list[2])
"""
Output :
apple
banana
cherry
"""
```

#### Negative Indexing
Negative indexing means start from the end

`-1` refers to the last item, `-2` refers to the second last item etc.
```py
# Example :
list1 = ["apple", "banana", "cherry"]
print(list1[-1])
print(list1[-2])

"""
Output : 
cherry
banana
"""
```

#### Range of Indexes
You can specify a range of indexes by specifying where to start and where to end the range.  
When specifying a range, the return value will be a new list with the specified items.
```py
#Example : Return the third, fourth, and fifth item:
list1 = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(list1[2:5])

#Output :  ['cherry', 'orange', 'kiwi']

list2 = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(list2[:4]) #By leaving out the start value, the range will start at the first item

#Output : ['apple', 'banana', 'cherry', 'orange']

list3 = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(list3[2:])  #By leaving out the end value, the range will go on to the end of the list

#Output : ['cherry', 'orange', 'kiwi', 'melon', 'mango']
```

#### Range of Negative Indexes
Specify negative indexes if you want to start the search from the end of the list:
```py
# Example : This example returns the items from "orange" (-4) to, but NOT including "mango" (-1):
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[-4:-1])

#Output : ['orange', 'kiwi', 'melon']
```
#### Check if Item Exists
To determine if a specified item is present in a list use the in keyword:
```py
# Example : Check if "apple" is present in the list:
l1 = ["apple", "banana", "cherry"]
if "apple" in l1:
  print("Yes, 'apple' is in the fruits list")
  
#Output : Yes, 'apple' is in the fruits list
```

#### Change Item Value
To change the value of a specific item, refer to the index number
```py
# Example : Change the second item:
l1 = ["apple", "banana", "cherry"]
l1[1] = "blackcurrant"
print(l1)

#Output : ['apple', 'blackcurrant', 'cherry']
```
#### Change a Range of Item Values
To change the value of items within a specific range, define a list with the new values,  
and refer to the range of index numbers where you want to insert the new values:
```py
# Example : Change the values "banana" and "cherry" with the values "blackcurrant" and "watermelon":
l1 = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
l1[1:3] = ["blackcurrant", "watermelon"]
print(l1)

# Output : ['apple', 'blackcurrant', 'watermelon', 'orange', 'kiwi', 'mango']

#Example : Change the second value by replacing it with two new values:
l2 = ["apple", "banana", "cherry"]
l2[1:2] = ["blackcurrant", "watermelon"]
print(l2)

#Output : ['apple', 'blackcurrant', 'watermelon', 'cherry']

# Example : Change the second and third value by replacing it with one value:
l3 = ["apple", "banana", "cherry"]
l3[1:3] = ["watermelon"]
print(l3)

#Output : ['apple', 'watermelon']
```

#### Python - List Methods
`List Methods`
Python has a set of built-in methods that you can use on lists.

- `append()`	Adds an element at the end of the list  
```py
#Example : Using the append() method to append an item:
l1 = ["apple", "banana", "cherry"]
l1.append("orange")
print(l1)

# Output : ['apple', 'banana', 'cherry', 'orange']
```
- `clear()`	Removes all the elements from the list  
```py
# Example : Clear the list content:
l1 = ["apple", "banana", "cherry"]
l1.clear()
print(l1)

#Output : []  #Empty List
```

- `copy()`	Returns a copy of the list  
```py
# Example : Copy the fruits list:
fruits = ['apple', 'banana', 'cherry', 'orange']
x = fruits.copy()
print(x)

#Output : ['apple', 'banana', 'cherry', 'orange']
```

- `count()`	Returns the number of elements with the specified value  
```py
#Example : Return the number of times the value "cherry" appears in the fruits list:
fruits = ['apple', 'banana', 'cherry']
x = fruits.count("cherry")
print(x)
#Output : 1

num =[1, 3, 7, 8, 7, 5, 4, 6, 8, 5]
x = num.count(5)
print(x)
#Output : 2
```

- `extend()`	Add the elements of a list (or any iterable), to the end of the current list  
```py
# Example : Add the elements of l2 to l1
l1 = ["apple", "banana", "cherry"]
l2 = ["mango", "pineapple", "papaya"]
l1.extend(l2)  #The elements will be added to the end of the list.
print(l1)

#Output : ['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya']

# Example : Add elements of a tuple to a list:
l1 = ["apple", "banana", "cherry"]
l2 = ("kiwi", "orange") 
print(type(l2)) 
l1.extend(l2)  #can add any iterable object (tuples, sets, dictionaries etc.)
print(l1)

"""
Output : 
<class 'tuple'>
['apple', 'banana', 'cherry', 'kiwi', 'orange']
"""
```

- `index()` Returns the index of the first element with the specified value  
```py
#Example : What is the position of the value "cherry":
fruits = ['apple', 'banana', 'cherry']
x = fruits.index("cherry")
print(x)

#Output : 2
```

- `insert()`	Adds an element at the specified position  
```py
#Example : Insert "watermelon" as the third item:
l1 = ["apple", "banana", "cherry"]
l1.insert(2, "watermelon")
print(l1)

#Output : ['apple', 'banana', 'watermelon', 'cherry']

# Example : Insert an item as the second position:
l2 = ["apple", "banana", "cherry"]
l2.insert(1, "orange")
print(l2)

#Output : ['apple', 'orange', 'banana',
```

- `pop()`	Removes the element at the specified position  
```py
# Example : Remove the second item:
l1 = ["apple", "banana", "cherry"]
l1.pop(1)
print(l1)

#Output : ['apple', 'cherry']

# Example : Remove the last item:

l2 = ["apple", "banana", "papaya" , "kiwi" , "cherry"]
l2.pop()  #If you do not specify the index, the pop() method removes the last item
print(l2)

#Output : ['apple', 'banana', 'papaya', 'kiwi']
```

- `remove()`	Removes the item with the specified value  
```py
# Example : Remove "cherry":
l1 = ["apple", "banana", "cherry"]
l1.remove("cherry")
print(l1)

#Output : ['apple', 'banana']
```

- `reverse()`	Reverses the order of the list  
```py
# Example : Reverse the order of the fruit list:
fruits = ['apple', 'banana', 'cherry']
fruits.reverse()
print(fruits)

#Output : ['cherry', 'banana', 'apple']
```

- `sort()`	Sorts the list  
```py
# Example : Reverse the order of the fruit list:
cars = ['Ford', 'BMW', 'Audi']
cars.sort()
print(cars)

#Output : ['Audi', 'BMW', 'Ford']
```

- `del` The del keyword also removes the specified index:
```py
# Example : Remove the first item:
l1 = ["apple", "banana", "cherry"]
del l1[0]
print(l1)

#Output : ['banana', 'cherry']

# Example : Delete the entire list:
l2 = ["apple", "banana", "cherry"]
del l2

#Output : Deletes the entire list 
```


## Python Tuples

```py
mytuple = ("apple", "banana", "cherry")
```
Tuples are used to store multiple items in a single variable.  
used to store collections of List, Set, and Dictionary, all with different qualities and usage.  
A tuple is a collection which is `ordered` and `unchangeable`.
Tuples are written with round brackets `()`.

```py
#Example : Create a Tuple:
mytuple = ("apple", "banana", "cherry")
print(mytuple)

#Output : ('apple', 'banana', 'cherry')
```

#### Tuple Items
Tuple items are `ordered`, `unchangeable`, and `allows duplicate values`.  
Tuple items are indexed, the first item has index [0], the second item has index [1] etc.

#### Ordered
When we say that tuples are ordered, it means that the items have a defined order, and that order will not change.

#### Unchangeable
Tuples are unchangeable, meaning that we cannot change, add or remove items after the tuple has been created.

#### Allow Duplicates
Since tuples are indexed, they can have items with the same value:
```py
# Example : Tuples allow duplicate values:
t1 = ("apple", "banana", "cherry", "apple", "cherry")
print(t1)

#Output : ('apple', 'banana', 'cherry', 'apple', 'cherry')
```

#### Tuple Length
To determine how many items a tuple has, use the len() function:
```py
# Example : Print the number of items in the tuple:
t1 = ("apple", "banana", "cherry")
print(len(t1))

#Output : 3
```

#### Create Tuple With One Item
To create a tuple with only one item, you have to add a comma',' after the item, otherwise Python will not recognize it as a tuple.
```py
# Example : One item tuple : 
t1 = ("apple",)  #remember the comma
print(type(t1))
#Output : <class 'tuple'>

#NOT a tuple
t2 = ("apple")
print(type(t2))
#Output : <class 'str'>
```

#### Tuple Items - Data Types
Tuple items can be of any data type and can contain different data types
```py
# Example : String, int and boolean data types:

tuple1 = ("apple", "banana", "cherry")
tuple2 = (1, 5, 7, 9, 3)
tuple3 = (True, False, False)
tuple4 = ("abc", 34, True, 40, "male")
print(tuple1)
print(tuple2)
print(tuple3)
print(tuple4)

"""
Output : 
('apple', 'banana', 'cherry')
(1, 5, 7, 9, 3)
(True, False, False)
('abc', 34, True, 40, 'male')
```

From Python's perspective, tuples are defined as objects with the data type :`<class 'tuple'>`
```py
# Example : What is the data type of a tuple?
mytuple = ("apple", "banana", "cherry")
print(type(mytuple))

#Output : <class 'tuple'>
```

#### `tuple()` Constructor
It is also possible to use the `tuple()` constructor to make a tuple.
```py
# Example : Using the tuple() method to make a tuple:
t1 = tuple(("apple", "banana", "cherry"))  #note the double round-brackets
print(t1)

#Output : <class 'tuple'>
```

#### Access Tuple Items
You can access tuple items by referring to the index number, inside square brackets`[]`
```py
# Example Print the second item in the tuple:
t1 = ("apple", "banana", "cherry")
print(t1[0])  #The first item has index 0.
print(t1[1]) 

"""
Output :
apple
banana
"""
```

#### Negative Indexing
Negative indexing means start from the end.
`-1` refers to the last item, `-2` refers to the second last item etc.
```py
# Example Print the last item of the tuple:
t1 = ("apple", "banana", "cherry")
print(t1[-1])

#Output : cherry
```

#### Range of Indexes
You can specify a range of indexes by specifying where to start and where to end the range.  
When specifying a range, the return value will be a new tuple with the specified items.
```py
# Example :  Return the third, fourth, and fifth item:
t1 = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(t1[2:5])  #The search will start at index 2 (included) and end at index 5 (not included)

#Output : ('cherry', 'orange', 'kiwi')

# Example : leaving out the start value, the range will start at the first item:
t2 = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(t2[:4])

#Output : ('apple', 'banana', 'cherry', 'orange')

# Example : leaving out the end value, the range will go on to the end of the list:
t3 = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(t3[2:])

#Output : ('cherry', 'orange', 'kiwi', 'melon', 'mango')
```

#### Range of Negative Indexes
Specify negative indexes if you want to start the search from the end of the tuple
```py
# Example : 
t1 = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(t1[-4:-1])

#Output : ('orange', 'kiwi', 'melon')
```

#### Check if Item Exists
```py
# Example : Check if "apple" is present in the tuple:
t1 = ("apple", "banana", "cherry")
if "apple" in t1:
  print("Yes, 'apple' is in the fruits tuple")

#Output : Yes, 'apple' is in the fruits tuple
```

#### Change Tuple Values
Once a tuple is created, you cannot change its values.  
Tuples are `unchangeable`, or immutable as it also is called.

But  You can convert the tuple into a list, change the list,  
and convert the list back into a tuple.
```py
# Example : 
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)

#Output : ("apple", "kiwi", "cherry")
```
#### Add Items
- Convert into a list:  

Just like the workaround for changing a tuple, you can convert it into a list, add your item(s), and convert it back into a tuple.
```py
# Example : Convert the tuple into a list, add "orange", and convert it back into a tuple:
t1 = ("apple", "banana", "cherry")
y = list(t1)
y.append("orange")
t1 = tuple(y)

#Output : ('apple', 'banana', 'cherry', 'orange')
```
- Add tuple to a tuple.  

You are allowed to add tuples to tuples, so if you want to add one item, (or many),  
create a new tuple with the item(s), and add it to the existing tuple.
```py
# Example : Create a new tuple with the value "orange", and add that tuple:
t1 = ("apple", "banana", "cherry")
y = ("orange",)
t1 += y
print(t1)

#Output: ('apple', 'banana', 'cherry', 'orange')
#Note: When creating a tuple with only one item, remember to include a comma after the item, otherwise it will not be identified as a tuple.
```

#### Remove Items
You cannot remove items in a tuple.  
but you can use the same workaround as we used for changing and adding tuple items:
```py
# Example : Convert the tuple into a list, remove "apple", and convert it back into a tuple:
x = ("apple", "banana", "cherry")
y = list(x)
y.remove("apple")
x = tuple(y)

#Output : ('banana', 'cherry')
```

#### Delete Tuple
```py
# Example : The del keyword can delete the tuple completely:
x = ("apple", "banana", "cherry")
del x
print(x) 

#Output : this will raise an error because the tuple no longer exists
```

#### Packing a Tuple
When we create a tuple, we normally assign values to it. This is called `packing` a tuple
```py
# Example : Packing a tuple:
fruits = ("apple", "banana", "cherry")

#Output : ('apple', 'banana', 'cherry')
```
#### Unpacking a Tuple
In Python, we are also allowed to extract the values back into variables.  
This is called `unpacking`.
```py
# Example :
fruits = ("apple", "banana", "cherry")
(a, b, c) = fruits
print(a)
print(b)
print(c)

"""
Output :
apple
banana
cherry
"""
```

#### Join Two Tuples
To join two or more tuples you can use the `+` operator:
```py
# Example : 
tuple1 = ("a", "b" , "c")
tuple2 = (1, 2, 3)
tuple3 = tuple1 + tuple2
print(tuple3)

#Output : ('a', 'b', 'c', 1, 2, 3)
```

#### Multiply Tuples
If you want to multiply the content of a tuple a given number of times,  
you can use the `*` operator:
```py
# Example :
fruits = ("apple", "banana", "cherry")
t1 = fruits * 2
print(t1)

#Output : ('apple', 'banana', 'cherry', 'apple', 'banana', 'cherry')
```

#### Tuple Methods
Python has two built-in methods that you can use on tuples.

- `count()`	Returns the number of times a specified value occurs in a tuple  
```py
# Example : Return the number of times the value 5 appears in the tuple:
t1 = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
x = t1.count(5)
print(x)

#Output : 2
```

- `index()`	Searches the tuple for a specified value and returns the position of where it was found  
```py
# Example : Search for the first occurrence of the value 8, and return its position:
t1 = (1, 3, 7, 8, 7, 5, 4, 6, 8, 5)
x = t1.index(8)
print(x)

#Output : 3
```


## Python Sets
```py
myset = {"apple", "banana", "cherry"}
```
Sets are used to store multiple items in a single variable.  
Set items are `unordered`, `unchangeable`, and `do not allow duplicate values` ,but you can remove items and add new items.  
Sets are written with curly brackets `{ }`.
```py
# Example : Create a Set:
s = {"apple", "banana", "cherry"}
print(s)

#Output : {'apple', 'cherry', 'banana'}
```

#### Unordered
Unordered means that the items in a set do not have a defined order therefore they cannot be referred to by index or key.

#### Unchangeable
Once a set is created, you cannot change its items, but you can remove items and add new items.

#### Duplicates Not Allowed
Sets cannot have two items with the same value.
```py
# Example : Duplicate values will be ignored:
s = {"apple", "banana", "cherry", "apple"}
print(s)

#output : {'banana', 'cherry', 'apple'}

# Example : True and 1 is considered the same value:
s1 = {"apple", "banana", "cherry", True, 1, 2}
print(s1)

#output : {True, 2, 'banana', 'cherry', 'apple'}
```

#### Length of a Set
To determine how many items a set has, use the `len()` function.
```py
# Example : Get the number of items in a set:
s1 = {"apple", "banana", "cherry"}
print(len(s1))

#Output : 3
```
#### Set Items - Data Types
Set items can be of any data type:
```py
# Example : String, int and boolean data types:
set1 = {"apple", "banana", "cherry"}
set2 = {1, 5, 7, 9, 3}
set3 = {True, False, False}
set4 = {"abc", 34, True, 40, "male"}   #A set can contain different data types
print(set1)
print(set2)
print(set3)
print(set4)

"""
Output :
{'apple', 'banana', 'cherry'}
{1, 3, 5, 7, 9}
{False, True}
{True, 34, 'abc', 40, 'male'}
"""
```

From Python's perspective, sets are defined as objects with the data type : `<class 'set'>`
```py
# Example : What is the data type of a set?
myset = {"apple", "banana", "cherry"}
print(type(myset))

#Output : <class 'set'>
```

#### `set()` Constructor
It is also possible to use the `set()` constructor to make a set.
```py
# Example : Using the set() constructor to make a set:
s = set(("apple", "banana", "cherry")) # note the double round-brackets
print(s)

#Output : {'apple', 'banana', 'cherry'}
```

#### Access Items
You cannot access items in a set by referring to an index or a key.  
But you can loop through the set items using a for loop, or ask if a specified value is present in a set, by using the `in` keyword.
```py
# Example : Loop through the set, and print the values:
s = {"apple", "banana", "cherry"}
for x in s:
  print(x)

"""
Output : 
banana
cherry
apple
"""

# Example : Check if "banana" is present in the set:
s1 = {"apple", "banana", "cherry"}
print("banana" in s1)

#Output : True
```

#### Set Methods

- `add()`	Adds an element to the set  
```py
# Example : Add an item to a set, using the add() method:
s = {"apple", "banana", "cherry"}
s.add("orange")
print(s)

#Output : {'banana', 'apple', 'cherry', 'orange'}
```

- `clear()`	Removes all the elements from the set  
```py
s = {"apple", "banana", "cherry"}
s.clear()
print(s)

#Output : set()
```

- `discard()`	Remove the specified item  
```py
#If the item to remove does not exist, discard() will NOT raise an error.
# Example : Remove "banana" by using the discard() method:
s = {"apple", "mango", "cherry"}
s.discard("banana")
print(s)

#Output : {'cherry', 'apple', 'mango'}
```

- `pop()`	Removes an element from the set  
```py
# Example : Remove a random item by using the pop() method:
s = {"apple", "banana", "cherry"}
x = s.pop()   #The return value of the pop() method is the removed item.
print(x)
print(s)

"""
Output :
banana
{'apple', 'cherry'}
"""
```

- `remove()`	Removes the specified element  
```py
# Example : Remove "banana" by using the remove() method:
s = {"apple", "banana", "cherry"}
s.remove("banana")
print(s)

#Output :{'apple', 'cherry'}

#If the item to remove does not exist, remove() will raise an error.
# Example : Remove "banana" by using the remove() method:
s = {"apple", "mango", "cherry"}
s.remove("banana")
print(s)

#Output : Error
```

- `union()`	Return a set containing the union of sets  
```py
# Example :
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3)

#Output : {'c', 1, 2, 3, 'a', 'b'}
```

- `update()`	Update the set with the union of this set and others  
```py
# Example : Add elements from x into s:
s = {"apple", "banana", "cherry"}
x = {"pineapple", "mango", "papaya"}
s.update(x)
print(s)

#Output : {'banana', 'papaya', 'mango', 'pineapple', 'cherry', 'apple'}

# Example : Add elements of a list to at set:
s = {"apple", "banana", "cherry"}
x = ["kiwi", "orange"]  
s.update(x)    #The object in the update() method can be any iterable object (tuples, lists, dictionaries etc.)
print(s)

#Output : {'orange', 'cherry', 'kiwi', 'banana', 'apple'}
```

- `del` will delete the set completely  
```py
# Example :
s = {"apple", "banana", "cherry"}
del s
print(s)

#Output : Deletes the set s
```

- `intersection()` will return a new set, that only contains the items that are present in both sets.  
```py
# Example : Return a set that contains the items that exist in both set x, and set y:
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
z = x.intersection(y)
print(z)

#Output : {'apple'}
```
