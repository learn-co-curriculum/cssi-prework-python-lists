
#Python Lists

#Objectives:
* Create a list using Python syntax
* Use list functions to add, remove, and modify a list

#Motivation:
In this lesson you will learn how to create Python's version of an array, a **list**. You will also learn how to use loops in your Python code in order to manipulate or use the elements in that list.

Code along with this readme in the Python console. To access the console, type 'python' into the command line. When you're finished, exit by typing 'quit()'

#Lists in Python
A list is the most basic Python data structure. It is a list of objects or values. The syntax for a list is the same as the syntax for an array in JavaScript: a set of objects enclosed in brackets.

To create an empty list, set a variable equal to empty brackets:
```
>>> empty_list = []
```
To create a list with some elements in it, just add the elements separated by commas:
```
>>> groceries = ['Eggs', 'Milk','Kale']
```
###Accessing List Items
List items have an index and are accessed using bracket notation. Just like in JavaScript, indexing starts at 0:

```
>>> groceries[0]
'Eggs'
>>> groceries[1]
'Milk'
>>> groceries[0:2]
['Eggs', 'Milk']
>>> groceries[1:]
['Milk', 'Kale']
```

###Modifying a List
The easiest way to modify a list’s content is to just access the list element by its index (numerical place in the list) and use the assignment operator. Lists are mutable, which means a list can be changed without being recreated. 
```
>>> groceries
['Eggs', 'Milk','Kale']
>>> groceries[0] = 'Bread'
>>> groceries
['Bread', 'Milk', 'Kale']
```

###Methods to Modify Lists

You can also modify lists using certain list-specific methods. 

#### `append()`
The append method allows you to stick an element at the end of a list. Note that `append()` only takes one argument.
```
>>> groceries.append('Asparagus')
>>> groceries
['Bread', 'Milk', 'Kale', 'Asparagus']
```
#### `extend()`
To add more than one element to an existing list, you can use `extend()` which will concatenate lists together.
```
>>>groceries.extend(['Rutabaga', 'Ice Cream'])
['Bread', 'Milk', 'Kale', 'Asparagus','Rutabaga', 'Ice Cream']
```
#### `del()`
You can use `del` to remove an element at a specific index.
```
>>>del groceries[3] #removes 'Asparagus' from the list
['Bread', 'Milk', 'Kale','Rutabaga', 'Ice Cream']
```

#### `remove()`
If you know the value that you'd like removed, you can use `remove()` which looks for the first matching value and removes it from a list.

```
>>>groceries.remove('Rutabaga')
['Bread','Milk','Kale','Ice Cream']
```

#### `sort()`
To order a list alphabetically or numerically use sort()
```
>>>groceries.sort()
['Bread', 'Ice Cream', 'Kale', 'Milk']
```

#### `len()`
The `len()` function returns the number of items in a list:
```
print len(groceries)
4
```
#### `insert()`
The `insert()` function inserts an item into a list at a specific location. It takes two arguments: The index, and the object to be inserted.

```
>>>groceries.insert(3, 'Marshmallows')
['Bread', 'Ice Cream', 'Kale', 'Marshmallows', 'Milk']
```

#### `pop()`
Removes the last item in the list and returns that value
```
>>>last_item=groceries.pop()
>>>last_item
'Milk'
>>>groceries
['Bread', 'Ice Cream', 'Kale', 'Marshmallows']
```

#### `reverse()`
Reverses the order of the entire list

```
>>>groceries.reverse()
['Marshmallows', 'Kale', 'Ice Cream', 'Bread']
```
#### `count()`
Counts how many times a value occurs in the list
```
bucket_list=['Paint', 'Chicken', 'Sand', 'Beer', 'Paint']
>>>bucket_list.count('Paint')
2
```

### 'In' and 'Not' Operators

You can use 'in' to check the condition that a value exists within a list.
```python
if 'Kale' in groceries:
  print "Thank goodness we're not missing out on this super food."
else:
  print 'Buy all the kale!'
```
To check if an element is absent from a list, use the 'not' in operator:
```python
if 'Milk' not in groceries:
  print "Don't forget the milk"
```

###Using range() to Build Lists
In testing a script, you might want to quickly generate a list of numbers. Rather than have you type out all the numbers you want, Python makes this easy with 'range()'. The syntax is `range(<start_int>, <end_int>, <interval>)` where the interval is an optional parameter and defaults to 1.

```
range(0,10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
range(0,100,10)
[0, 10, 20, 30, 40, 50, 60, 70, 80, 90]
```
