
#Python Lists and Loops

#Objectives:
* Create a list in Python syntax
* Create a for loops and while loops in Python syntax

#Motivation:
In this lesson you will learn how to create Python's version of an array, a list. You will also learn how to use loops in your Python code in order to manipulate or use the elements in that list.

#Lists in Python
A list is the most basic Python data structure. It is a list of objects or values. The syntax for a list is the same as the syntax for an array in JavaScript: a set of objects enclosed in brackets. You should code-along in the Python console. To access this, your just have to type 'python' into the command line. When you're finished, exit by typing 'quit()'

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
The easiest way to modify a list’s content is to just access the list element by its index (numerical place in the list) and use the assignment operator.
```
>>> groceries
['Eggs', 'Milk','Kale']
>>> groceries[0] = 'Bread'
>>> groceries
['Bread', 'Milk', 'Kale']
```

###Methods to Modify Lists

You can also modify lists using certain list-specific methods.

The append method allows you to stick an element at the end of a list. Note that `append()` only takes one argument.
```
>>> groceries.append('Asparagus')
>>> groceries
['Bread', 'Milk', 'Kale', 'Asparagus']
```

To add more than one element to an existing list, you can use `extend()` which will concatenate lists together.
```
groceries.extend(['Rutabaga', 'Ice Cream'])
['Bread', 'Milk', 'Kale', 'Asparagus','Rutabaga', 'Ice Cream']
```

You can use `del` to remove an element at a specific index.
```
del groceries[3] #removes 'Asparagus' from the list
['Bread', 'Milk', 'Kale','Rutabaga', 'Ice Cream']
```
If you know the value that you'd like removed, you can use `remove()` which looks for the first matching value and removes it from a list.

```
groceries.remove('Rutabaga')
['Bread','Milk','Kale','Ice Cream']
```

To order a list alphabetically or numerically use sort()
```
groceries.sort()
['Bread', 'Ice Cream', 'Kale', 'Milk']
```


Finally, the `len()` function, you can return the number of items in a list:
```
print len(groceries)
3
```

### 'In' and 'Not' Operators

You can use 'in' to check the condition that a value exists within a list.
```python
if 'Kale' in groceries:
  print "Thank gosh we're not missing out on this super food."
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


#Loops
Loops are a common tool is any programing language that let us repeat a section of code over and over, even if we only type it out once. You have already seen loops once in JavaScript, and now that you understand Python's list syntax, it's important to be able to iterate over each item in a list, or (as you'll learn in the next lesson) over other datatypes.


###For Loops
The simplest looping situation is where you need to do something _for_ a certain number of times. In this case, the number of iterations is known. To do this, Python uses a for loop.

##### Example 1: Looping Through a List

This code will repeat for every element in the list.

```python
for name in ["Lucy", "Ricky", "Ricky Jr."]:
  print name
```
Note that the variable `name` is what we are calling each element within the list. We could call that variable anything: `character`, `person`, `actor`. It doesn't matter, as long as we continue to use that variable later within the _for_ block.

Alternatively, we can declare a variable `names` which contains a list of all three members in the Ricardo family, and then use the same syntax.
```python
#same result, slightly different syntax
names = ["Lucy", "Ricky", "Ricky Jr."]
for person in names:
  print person
```
##### Example 2: Looping through Integers

The _for_ loop syntax is similar for integers. In the example below, string interpolation (a jargony word that means substitution) is used. The curly brackets act as a placeholder. The .format() method that is chained to the end of the string indicating which value should be substituted into the placeholder.

```python
for i in range(1, 4):
  print "I am looping and am currently on {}.".format(i)
```

You can also declare your variable before the loop. And while `i` is the most common variable name for iteration, any variable name can be used.

```
my_range = range(2,5)
for num in my_range:
  print "Did you know that {} times 2 is {}.".format(num, num*2)
```
###While Loops
While loops continue to repeat _while_ - or as long as - a certain condition is met. While loops are used when we're not sure how many iterations (if any) might occur.

##### Example 1: A Simple While Loop
This code will repeat while the condition `n<5` is met. It will stop when n is equal to 5.

```python
n = 0
while n < 5:
  print n
  n = n + 1
```
##### Example 2: A While/Else Loop
While/Else is a loop type that does not exist in JavaScript. Once a condition is no longer true, the code block inside the else statement is executed.

In this case, once `n<5` is not met, the instructions in the `else` block are executed. Then, the entire _while_ loop is exited, and the next instruction (to print `"You counted to 5"`) is executed.
```python
n = 0
while n < 5:
  print n, " is  less than 5"
  n = n + 1
else:
  print n, " is not less than 5"

print "You counted to 5"
```

#Conclusion
Creating, modifying and accessing lists are important for every programmer, as is being able to use _for_ loops and _while_ loops. Practicing these small examples are a great way to build your foundation as a strong developer and will prepare you for the next lab.
