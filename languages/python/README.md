
# Python 3 Tutorial

Python is a powerful programming language ideal for scripting and rapid application development. It is used in web development (like: Django and Bottle), scientific and mathematical computing (Orange, SymPy, NumPy) to desktop graphical user Interfaces (Pygame, Panda3D).

This tutorial introduces you to the basic concepts and features of Python 3. After reading the tutorial, you will be able to read and write basic Python programs, and explore Python in depth on your own.

This tutorial is intended for people who have knowledge of other programming languages and want to get started with Python quickly.

----------

## Python for Beginners

If you are a programming newbie, we suggest you to visit:

1.  **[Python Programming](https://www.programiz.com/python-programming "Python programming")**  - A comprehensive guide on what's Python, how to get started in Python, why you should learn it, and how you can learn it.
2.  **Python Tutorials**  - Follow sidebar links one by one.
3.  **[Python Examples](https://www.programiz.com/python-programming/examples "Python example")**  - Simple examples for beginners to follow.

----------

## What's covered in this tutorial?

-   [Run Python on your computer](https://www.programiz.com/python-programming/tutorial#install)
-   [Introduction (Variables, Operators, I/O, ...)](https://www.programiz.com/python-programming/tutorial#introduction)
-   [Data Structures (List, Dictionary, Set, ...)](https://www.programiz.com/python-programming/tutorial#data-structure)
-   [Control Flow (if, loop, break, ...)](https://www.programiz.com/python-programming/tutorial#control-flow)
-   [File (File Handling, Directory, ...)](https://www.programiz.com/python-programming/tutorial#file)
-   [Exceptions (Handling, User-defined Exception, ...)](https://www.programiz.com/python-programming/tutorial#exception)
-   [OOP (Object & Class, Inheritance, Overloading, ...)](https://www.programiz.com/python-programming/tutorial#oop)
-   [Standard Library (Built-in Function, List Methods, ...)](https://www.programiz.com/python-programming/tutorial#standard%20library)
-   [Misc (Generators, decorators, ...)](https://www.programiz.com/python-programming/tutorial#misc)

----------

## Run Python on Your computer

You do not need to install Python on your computer to follow this tutorial. However, we recommend you to run Python programs included in this tutorial on your own computer.

-   [Run Python on Windows](https://docs.python.org/3/using/windows.html)
-   [Run Python on MacOS](https://docs.python.org/3/using/mac.html)

## Python Introduction

Let's write our first Python program, "Hello, World!". It's a simple program that prints  Hello World!  on the standard output device (screen).

----------

### "Hello, World!" Program

```python
print("Hello, World!")
```

Run Code

When you run the program, the output will be:

Hello, World!

In this program, we have used the built-in  [print()](https://www.programiz.com/python-programming/methods/built-in/print)  function to print  Hello, world!  string.

----------

### Variables and Literals

A variable is a named location used to store data in the memory. Here's an example:

```python
a = 5  

```

Here,  a  is a variable. We have assigned  `5`  to variable  a

We do not need to define variable type in Python. You can do something like this:

```python
a = 5
print("a =", 5)
a = "High five"
print("a =", a)
```

Run Code

Initially, integer value  `5`  is assigned to the variable  a. Then, the string  High five  is assigned to the same variable.

By the way,  `5`  is a numeric literal and  `"High five"`  is a string literal.

When you run the program, the output will be:

a = 5
a = High five 

Visit  [Python Variables, Constants and Literals](https://www.programiz.com/python-programming/variables-constants-literals "Python Constans and Variables")  to learn more.

----------

### Operators

Operators are special symbols that carry out operations on operands (variables and values).

Let's talk about arithmetic and assignment operators in this part.

Arithmetic operators are used to perform mathematical operations like addition, subtraction, multiplication etc.

```python
x = 14
y = 4

# Add two operands
print('x + y =', x+y) # Output: x + y = 18

# Subtract right operand from the left
print('x - y =', x-y) # Output: x - y = 10

# Multiply two operands
print('x * y =', x*y) # Output: x * y = 56

# Divide left operand by the right one 
print('x / y =', x/y) # Output: x / y = 3.5

# Floor division (quotient)
print('x // y =', x//y) # Output: x // y = 3

# Remainder of the division of left operand by the right
print('x % y =', x%y) # Output: x % y = 2

# Left operand raised to the power of right (x^y)
print('x ** y =', x**y) # Output: x ** y = 38416
```

Run Code

Assignment operators are used to assign values to variables. You have already seen the use of  `=`  operator. Let's try some more assignment operators.

```python
x = 5

# x += 5 ----> x = x + 5
x +=5
print(x) # Output: 10

# x /= 5 ----> x = x / 5
x /= 5
print(x) # Output: 2.0
```

Run Code

Other commonly used assignment operators:  `-=`,  `*=`,  `%=`,  `//=`  and  `**=`.

Visit  [Python Operators](https://www.programiz.com/python-programming/operators)  to learn about all operators in detail.

----------

### Get Input from User

In Python, you can use  [input() function](https://www.programiz.com/python-programming/methods/built-in/input)  to take input from user. For example:

```python
inputString = input('Enter a sentence:')
print('The inputted string is:', inputString)

```

When you run the program, the output will be:

Enter a sentence: Hello there.
The inputted string is: Hello there. 

----------

### Python Comments

There are 3 ways of creating comments in Python.

# This is a comment

  """This is a 
    multiline
    comment."""

  '''This is also a
     multiline
     comment.'''

To learn more about comments and docstring, visit:  [Python Comments](https://www.programiz.com/python-programming/statement-indentation-comments#comments "Python Comments").

----------

### Type Conversion

The process of converting the value of one data type (integer, string, float, etc.) to another is called type conversion. Python has two types of type conversion.

**Implicit Type Conversion**

Implicit conversion doesn't need any user involvement. For example:

```python
num_int = 123  # integer type
num_flo = 1.23 # float type

num_new = num_int + num_flo

print("Value of num_new:",num_new)
print("datatype of num_new:",type(num_new))
```

Run Code

When you run the program, the output will be:

Value of num_new: 124.23
datatype of num_new: datatype of num_new: <class 'float'>

Here,  num_new  has float data type because Python always converts smaller data type to larger data type to avoid the loss of data.

Here is an example where Python interpreter cannot implicitly type convert.

```python
num_int = 123     # int type
num_str = "456"   # str type

print(num_int+num_str)
```

Run Code

When you run the program, you will get

TypeError: unsupported operand type(s) for +: 'int' and 'str'

However, Python has a solution for this type of situation which is know as explicit conversion.

**Explicit Conversion**

In case of explicit conversion, you convert the datatype of an object to the required data type. We use predefined functions like  [int()](https://www.programiz.com/python-programming/methods/built-in/int),  [float()](https://www.programiz.com/python-programming/methods/built-in/float),  [str()](https://www.programiz.com/python-programming/methods/built-in/str)  etc. to perform explicit type conversion. For example:

```python
num_int = 123  # int type
num_str = "456" # str type

# explicitly converted to int type
num_str = int(num_str) 

print(num_int+num_str)
```

Run Code

To lean more, visit  [Python type conversion](https://www.programiz.com/python-programming/type-conversion-and-casting).

----------

### Python Numeric Types

Python supports integers, floating point numbers and complex numbers. They are defined as  `int`,  `float`  and  `complex`  class in Python. In addition to that, booleans:  `True`  and  `False`  are a subtype of integers.

```python
# Output: <class 'int'>
print(type(5))

# Output: <class 'float'>
print(type(5.0))

c = 5 + 3j

# Output: <class 'complex'>
print(type(c))
```

Run Code

To learn more, visit  [Python Number Types](https://www.programiz.com/python-programming/numbers).

----------

## Python Data Structures

Python offers a range of compound datatypes often referred to as sequences. You will learn about those built-in types in this section.

----------

### Lists

A list is created by placing all the items (elements) inside a square bracket  `[]`  separated by commas.

It can have any number of items and they may be of different types (integer, float, string etc.)

```python
# empty list
my_list = []

# list of integers
my_list = [1, 2, 3]

# list with mixed data types
my_list = [1, "Hello", 3.4]

```

You can also use  [list() function](https://www.programiz.com/python-programming/methods/built-in/list "Python lists() function")  to create lists.

Here's how you can access elements of a list.

```python
language = ["French", "German", "English", "Polish"]

# Accessing first element
print(language[0])


# Accessing fourth element
print(language[3])
```

Run Code

You use the index operator  `[]`  to access an item in a list. Index starts from 0. So, a list having 10 elements will have index from 0 to 9.

Python also allows negative indexing for its sequences. The index of -1 refers to the last item, -2 to the second last item and so on.

Check these resources for more information about Python lists:

-   [Python lists (slice, add and remove item etc.)](https://www.programiz.com/python-programming/methods/list)
-   [Python list methods](https://www.programiz.com/python-programming/methods/list)
-   [Python list comprehension](https://www.programiz.com/python-programming/list-comprehension)

----------

### Tuples

Tuple is similar to a list except you cannot change elements of a tuple once it is defined. Whereas in a list, items can be modified.

Basically, list is mutable whereas tuple is immutable.

```python
language = ("French", "German", "English", "Polish")
print(language)
```

Run Code

You can also use  [tuple() function](https://www.programiz.com/python-programming/methods/built-in/tuple "Python tuple() function")  to create tuples.

You can access elements of a tuple in a similar way like a list.

```python
language = ("French", "German", "English", "Polish")

print(language[1]) #Output: German
print(language[3]) #Output: Polish
print(language[-1]) # Output: Polish
```

Run Code

You cannot delete elements of a tuple, however, you can entirely delete a tuple itself using  `del`  operator.

```python
language = ("French", "German", "English", "Polish")
del language

# NameError: name 'language' is not defined
print(language)
```

Run Code

To learn more, visit  [Python Tuples](https://www.programiz.com/python-programming/tuple).

----------

### String

A string is a sequence of characters. Here are different ways to create a string.

```python
# all of the following are equivalent
my_string = 'Hello'
print(my_string)

my_string = "Hello"
print(my_string)

my_string = '''Hello'''
print(my_string)

# triple quotes string can extend multiple lines
my_string = """Hello, welcome to
           the world of Python"""
print(my_string)
```

Run Code

You can access individual characters of a string using indexing (in a similar manner like lists and tuples).

```python
str = 'programiz'
print('str = ', str)

print('str[0] = ', str[0]) # Output: p

print('str[-1] = ', str[-1]) # Output: z

#slicing 2nd to 5th character
print('str[1:5] = ', str[1:5]) # Output: rogr

#slicing 6th to 2nd last character
print('str[5:-2] = ', str[5:-2]) # Output: am
```

Run Code

Strings are immutable. You cannot change elements of a string once it is assigned. However, you can assign one string to another. Also, you can delete the string using  `del`  operator.

Concatenation is probably the most common string operation. To concatenate strings, you use  `+`  operator. Similarly, the  `*`  operator can be used to repeat the string for a given number of times.

```python
str1 = 'Hello '
str2 ='World!'

# Output: Hello World!
print(str1 + str2)

# Hello Hello Hello
print(str1 * 3)
```

Run Code

Check these resources for more information about Python strings:

-   [Python Strings](https://www.programiz.com/python-programming/string "Python Strings")
-   [Python String Methods](https://www.programiz.com/python-programming/methods/string "Python String Methods")
-   [Python String Formatting](https://www.programiz.com/python-programming/methods/string/format "Python String format()")

----------

### Sets

A set is an unordered collection of items where every element is unique (no duplicates).

Here is how you create sets in Python.

```python
# set of integers
my_set = {1, 2, 3}
print(my_set)

# set of mixed datatypes
my_set = {1.0, "Hello", (1, 2, 3)}
print(my_set)
```

Run Code

You can also use  [set()](https://www.programiz.com/python-programming/methods/built-in/set)  function to create sets.

Sets are mutable. You can add, remove and delete elements of a set. However, you cannot replace one item of a set with another as they are unordered and indexing have no meaning.

Let's try commonly used set methods:  [add()](https://www.programiz.com/python-programming/methods/set/add "Python set add()"),  [update()](https://www.programiz.com/python-programming/methods/set/update)  and  [remove()](https://www.programiz.com/python-programming/methods/set/remove).

```python
# set of integers
my_set = {1, 2, 3}

my_set.add(4)
print(my_set) # Output: {1, 2, 3, 4}

my_set.add(2)
print(my_set) # Output: {1, 2, 3, 4}

my_set.update([3, 4, 5])
print(my_set) # Output: {1, 2, 3, 4, 5}

my_set.remove(4)
print(my_set) # Output: {1, 2, 3, 5}
```

Run Code

Let's tryout some commonly used set operations:

```python
A = {1, 2, 3}
B = {2, 3, 4, 5}

# Equivalent to A.union(B) 
# Also equivalent to B.union(A)
print(A | B) # Output: {1, 2, 3, 4, 5}

# Equivalent to A.intersection(B)
# Also equivalent to B.intersection(A)
print (A & B) # Output: {2, 3}

# Set Difference
print (A - B) # Output: {1}

# Set Symmetric Difference
print(A ^ B)  # Output: {1, 4, 5}
```

Run Code

**More Resources:**

-   [Python Sets](https://www.programiz.com/python-programming/set "Python Sets")
-   [Python Set Methods](https://www.programiz.com/python-programming/methods/set "Python Set Methods")
-   [Python Frozen Set](https://www.programiz.com/python-programming/methods/built-in/frozenset "Python Frozen Set")

----------

### Dictionaries

Dictionary is an unordered collection of items. While other compound data types have only value as an element, a dictionary has a  `key: value`  pair. For example:

```python
# empty dictionary
my_dict = {}

# dictionary with integer keys
my_dict = {1: 'apple', 2: 'ball'}

# dictionary with mixed keys
my_dict = {'name': 'John', 1: [2, 4, 3]}
```

Run Code

You can also use  [dict()](https://www.programiz.com/python-programming/methods/built-in/dict "Python dict() to create a dictionary")  function to create dictionaries.

To access value from a dictionary, you use key. For example:

```python
person = {'name':'Jack', 'age': 26, 'salary': 4534.2}
print(person['age']) # Output: 26
```

Run Code

Here's how you can change, add or delete dictionary elements.

```python
person = {'name':'Jack', 'age': 26}

# Changing age to 36
person['age'] = 36 
print(person) # Output: {'name': 'Jack', 'age': 36}

# Adding salary key, value pair
person['salary'] = 4342.4
print(person) # Output: {'name': 'Jack', 'age': 36, 'salary': 4342.4}


# Deleting age
del person['age']
print(person) # Output: {'name': 'Jack', 'salary': 4342.4}

# Deleting entire dictionary
del person
```

Run Code

**More resources:**

-   [Python Dictionary](https://www.programiz.com/python-programming/dictionary)
-   [Python Dictionary Methods](https://www.programiz.com/python-programming/methods/dictionary)
-   [Python Dictionary Comprehension](https://www.datacamp.com/community/tutorials/python-dictionary-comprehension)

----------

### Python range()

`range()`  returns an immutable sequence of numbers between the given start integer to the stop integer.

```python

print(range(1, 10)) # Output: range(1, 10)

```

The output is an iterable and you can convert it to list, tuple, set and so on. For example:

```python
numbers = range(1, 6)

print(list(numbers)) # Output: [1, 2, 3, 4, 5]
print(tuple(numbers)) # Output: (1, 2, 3, 4, 5)
print(set(numbers)) # Output: {1, 2, 3, 4, 5}

# Output: {1: 99, 2: 99, 3: 99, 4: 99, 5: 99} 
print(dict.fromkeys(numbers, 99))
```

Run Code

We have omitted optional  `step`  parameter for  `range()`  in above examples. When omitted,  `step`  defaults to 1. Let's try few examples with  `step`  parameter.

```python
# Equivalent to: numbers = range(1, 6)
numbers1 = range(1, 6 , 1)
print(list(numbers1)) # Output: [1, 2, 3, 4, 5]

numbers2 = range(1, 6, 2)
print(list(numbers2)) # Output: [1, 3, 5]

numbers3 = range(5, 0, -1)
print(list(numbers3)) # Output: [5, 4, 3, 2, 1]
```

Run Code

----------

## Python Control Flow

----------

### if...else Statement

The  `if...else`  statement is used if you want perform different action (run different code) on different condition. For example:

```python
num = -1

if num > 0:
    print("Positive number")
elif num == 0:
    print("Zero")
else:
    print("Negative number")
    
# Output: Negative number
```

Run Code

There can be zero or more  `elif`  parts, and the  `else`  part is optional.

Most programming languages use  `{}`  to specify the block of code. Python uses indentation.

A code block starts with indentation and ends with the first unindented line. The amount of indentation is up to you, but it must be consistent throughout that block.

Generally, four whitespace is used for indentation and is preferred over tabs.

Let's try another example:

```python
if False:
  print("I am inside the body of if.")
  print("I am also inside the body of if.")
print("I am outside the body of if")

# Output: I am outside the body of if.
```

Run Code

Before you move on to next section, we recommend you to check  [comparison operator](https://www.programiz.com/python-programming/operators#comparison)  and  [logical operator](https://www.programiz.com/python-programming/operators#logical).

Also, check out  [Python if...else](https://www.programiz.com/python-programming/if-elif-else)  in detail.

----------

### while Loop

Like most programming languages,  `while`  loop is used to iterate over a block of code as long as the test expression (condition) is  `true`. Here is an example to find the sum of natural numbers:

```python
n = 100

# initialize sum and counter
sum = 0
i = 1

while i <= n:
    sum = sum + i
    i = i+1    # update counter

print("The sum is", sum)

# Output: The sum is 5050
```

Run Code

In Python, while loop can have optional  `else`  block that is executed if the condition in the  `while`  loop evaluates to  `False`. However, if the loop is terminated with  `break`  statement, Python interpreter ignores the  `else`  block.

To learn more, visit  [Python while Loop](https://www.programiz.com/python-programming/while-loop "Python while Loop")

----------

### for Loop

In Python,  `for`  loop is used to iterate over a sequence (list, tuple, string) or other iterable objects. Iterating over a sequence is called traversal.

Here's an example to find the sum of all numbers stored in a list.

```python
numbers = [6, 5, 3, 8, 4, 2]

sum = 0

# iterate over the list
for val in numbers:
  sum = sum+val

print("The sum is", sum) # Output: The sum is 28
```

Run Code

Notice the use of  `in`  operator in the above example. The  `in`  operator returns  `True`  if value/variable is found in the sequence.

In Python,  `for`  loop can have optional  `else`  block. The else part is executed if the items in the sequence used in  `for`  loop exhausts. However, if the loop is terminated with  `break`  statement, Python interpreter ignores the  `else`  block.

To learn more, visit  [Python for Loop](https://www.programiz.com/python-programming/for-loop "Python for Loop")

----------

### break Statement

The break statement terminates the loop containing it. Control of the program flows to the statement immediately after the body of the loop. For example:

```python
for val in "string":
    if val == "r":
        break
    print(val)

print("The end")
```

Run Code

When you run the program, the output will be:

s
t
The end 

----------

### continue Statement

The continue statement is used to skip the rest of the code inside a loop for the current iteration only. Loop does not terminate but continues on with the next iteration. For example:

```python
for val in "string":
    if val == "r":
        continue
    print(val)

print("The end")
```

Run Code

When you run the program, the output will be:

s
t
i
n
g
The end 

To learn more on  `break`  and  `continue`  with detail explanation, visit  [Python break and continue](https://www.programiz.com/python-programming/break-continue).

----------

### pass Statement

Suppose, you have a loop or a function that is not implemented yet, but want to implement it in the future. They cannot have an empty body. The interpreter would complain. So, you use the  `pass`  statement to construct a body that does nothing.

```python
sequence = {'p', 'a', 's', 's'}
for val in sequence:
    pass
```

Run Code

----------

## Python Function

A function is a group of related statements that perform a specific task. You use  `def`  keyword to create functions in Python.

```python
def print_lines():
  print("I am line1.")
  print("I am line2.")

```

You have to call the function to run the codes inside it. Here's how:

```python
def print_lines():
  print("I am line1.")
  print("I am line2.")

# function call
print_lines()
```

Run Code

A function can accept arguments.

```python
def add_numbers(a, b):
  sum = a + b
  print(sum)

add_numbers(4, 5)

# Output: 9
```

Run Code

You can also return value from a function using  `return`  statement.

```python
def add_numbers(a, b):
  sum = a + b
  return sum

result = add_numbers(4, 5)
print(result)

# Output: 9
```

Run Code

Here are few resources to check:

-   [Python Function](https://www.programiz.com/python-programming/function)
-   [Python Function Arguments (Default, Keyword, Arbitrary)](https://www.programiz.com/python-programming/function-argument)

----------

### Recursion (Recursive function)

A function that calls itself is known as recursive function and this process is called recursion.

Every recursive function must have a base condition that stops the recursion or else the function calls itself infinitely.

```python
# Recursive function to find the factorial of a number

def calc_factorial(x):

    if x == 1:
        return 1
    else:
        return (x * calc_factorial(x-1))

num = 6
print("The factorial of", num, "is", calc_factorial(num)) 

# Output: The factorial of 6 is 720
```

Run Code

Visit  [Python recursion](https://www.programiz.com/python-programming/recursion "Python Recursive Function")  to learn more.

----------

### Lambda Function

In Python, you can define functions without a name. These functions are called lambda or anonymous function. To create a lambda function,  `lambda`  keyword is used.

```python
square = lambda x: x ** 2
print(square(5))

# Output: 25
```

Run Code

We use lambda functions when we require a nameless function for a short period of time. Lambda functions are used along with built-in functions like  `filter()`,  `map()`  etc.

To learn more, visit:

-   [Python Lambda Function](https://www.programiz.com/python-programming/anonymous-function)
-   [Python map()](https://www.programiz.com/python-programming/methods/built-in/map)
-   [Python filter()](https://www.programiz.com/python-programming/methods/built-in/filter)

----------

### Modules

Modules refer to a file containing Python statements and definitions.

A file containing Python code, for e.g.:  `example.py`, is called a module and its module name would be  `example`.

Let us create it and save it as  `example.py`.

```python
# Python Module example

def add(a, b):
   return a + b

```

To use this module, we use  `import`  keyword.

```python
# importing example module
import example 

# accessing the function inside the module using . operator
example.add(4, 5.5) 

```python

Python has a ton of standard modules readily available for use. For example:

```python
import math

result = math.log2(5) # return the base-2 logarithm
print(result) # Output: 2.321928094887362
```

Run Code

You can import specific names from a module without importing the module as a whole. Here is an example.

```python
from math import pi
print("The value of pi is", pi)

# Output: The value of pi is 3.141592653589793
```

Run Code

**More Resources:**

-   [Python Modules](https://www.programiz.com/python-programming/modules)
-   [Python Packages](https://www.programiz.com/python-programming/package)

----------

## Python File I/O

A file operation takes place in the following order.

1.  Open a file
2.  Read or write (perform operation)
3.  Close the file

----------

### How to open a file?

You can use  [open()](https://www.programiz.com/python-programming/methods/built-in/open)  function to open a file.

```python
f = open("test.txt")    # open file in current directory
f = open("C:/Python33/README.txt")  # specifying full path

```

We can specify the mode while opening a file.

Mode

Description

'r'

Open a file for reading. (default)

'w'

Open a file for writing. Creates a new file if it does not exist or truncates the file if it exists.

'x'

Open a file for exclusive creation. If the file already exists, the operation fails.

'a'

Open for appending at the end of the file without truncating it. Creates a new file if it does not exist.

't'

Open in text mode. (default)

'b'

Open in binary mode.

'+'

Open a file for updating (reading and writing)

```python
f = open("test.txt")      # equivalent to 'r' or 'rt'
f = open("test.txt",'w')  # write in text mode
f = open("img.bmp",'r+b') # read and write in binary mode

```

----------

### How to close a file?

To close a file, you use  `close()`  method.

```python
f = open("test.txt",encoding = 'utf-8')
# perform file operations
f.close()

```

----------

### How to write to a file?

In order to write into a file in Python, we need to open it in write  `'w'`, append  `'a'`  or exclusive creation  `'x'`  mode.

```python
with open("test.txt",'w',encoding = 'utf-8') as f:
   f.write("my first file\n")
   f.write("This file\n\n")
   f.write("contains three lines\n")

```

Here, we have used  `with`  statement to open a file. This ensures that the file is closed when the block inside with is exited.

----------

### How to read files?

To read a file in Python, you must open the file in reading mode.

There are various methods available for this purpose. We can use the  `read(size)`  method to read in size number of data.

```python
f = open("test.txt",'r',encoding = 'utf-8')
f.read(4)    # read the first 4 data

```

Visit  [Python File I/O](https://www.programiz.com/python-programming/file-operation)  to learn more.

----------

### Python Directory

A directory or folder is a collection of files and sub directories. Python has the  [os module](https://docs.python.org/3/library/os.html), which provides many useful methods to work with directories and files.

```python
import os

os.getcwd()  // present working directory
os.chdir('D:\\Hello') // Changing current directory to D:\Hello
os.listdir()  // list all sub directories and files in that path
os.mkdir('test') // making a new directory test
os.rename('test','tasty') // renaming the directory test to tasty
os.remove('old.txt')  // deleting old.txt file

```

Visit  [Python Directory](https://www.programiz.com/python-programming/directory)  to learn more.

----------

## Python Exception Handling

Errors that occur at runtime are called exceptions. They occur, for example, when a file we try to open does not exist  `FileNotFoundError`, dividing a number by zero  `ZeroDivisionError`  etc.

Visit this page to learn about all  [built-in exceptions in Python](https://www.programiz.com/python-programming/exceptions).

If exceptions are not handled, an error message is spit out and our program come to a sudden, unexpected halt.

----------

In Python, exceptions can be handled using  `try`  statement. When exceptions are caught, it's up to you what operator to perform.

```python
# import module sys to get the type of exception
import sys

randomList = ['a', 0, 2]

for entry in randomList:
    try:
        print("The entry is", entry)
        r = 1/int(entry)
        break
    except:
        print("Oops!",sys.exc_info()[0],"occurred.")
        print("Next entry.")
        print()
print("The reciprocal of",entry,"is",r)
```

Run Code

When you run the program, the output will be:

The entry is a
Oops! <class 'ValueError'> occurred.
Next entry.

The entry is 0
Oops! <class 'ZeroDivisionError'> occurred.
Next entry.
    
The entry is 2
The reciprocal of 2 is 0.5

To learn about catching specific exceptions and  `finally`  clause with  `try`  statement, visit  [Python exception handling](https://www.programiz.com/python-programming/exception-handling).

Also, you can create user-defined exceptions in Python. For that, visit  [Python Custom Exceptions](https://www.programiz.com/python-programming/user-defined-exception)

----------

## Python OOP

Everything in Python is an object including integers, floats, functions, classes, and  `None`. Let's not focus on why everything in Python is an object. For that, visit  [this page](https://stackoverflow.com/questions/865911/is-everything-an-object-in-python-like-ruby). Rather, this section focuses on creating your own classes and objects.

----------

### Class and Objects

Object is simply a collection of data (variables) and methods (functions) that act on data. And, class is a blueprint for the object.

----------

### How to define a class?

```
class MyClass:
   a = 10
   def func(self):
      print('Hello')  

```

As soon as you define a class, a new class object is created with the same name. This class object allows us to access the different attributes as well as to instantiate new objects of that class.

```
class MyClass:
  "This is my class"
  a = 10
  def func(self):
    print('Hello')

# Output: 10
print(MyClass.a)

# Output: <function myclass.func at 0x7f04d158b8b0>
print(MyClass.func)

# Output: 'This is my class'
print(MyClass.__doc__)
```

Run Code

You may have noticed the  `self`  parameter in function definition inside the class but, we called the method simply as  `ob.func()`  without any arguments. It still worked.

This is because, whenever an object calls its method, the object itself is passed as the first argument. So,  `ob.func()`  translates into  `MyClass.func(ob)`.

----------

### Creating Objects

You can also create objects of the class yourself.

```
class MyClass:
  "This is my class"
  a = 10
  def func(self):
    print('Hello')

obj1 = MyClass()
print(obj1.a)        # Output: 10
 
obj2 = MyClass()
print(obj1.a + 5)    # Output: 15
```

Run Code

----------

### Python Constructors

In Python, a method with name  `__init()__`  is a constructor. This method is automatically called when an object is instantiated.

```
class ComplexNumber:
    def __init__(self,r = 0,i = 0):  # constructor
        self.real = r
        self.imag = i

    def getData(self):
        print("{0}+{1}j".format(self.real,self.imag))


c1 = ComplexNumber(2,3) # Create a new ComplexNumber object
c1.getData() # Output: 2+3j

c2 = ComplexNumber() # Create a new ComplexNumber object
c2.getData() # Output: 0+0j
```

Run Code

Visit  [Python Class and Object](https://www.programiz.com/python-programming/class)  to learn more.

----------

### Python Inheritance

Inheritance refers to defining a new class with little or no modification to an existing class. Let's take an example:

```
class Mammal:
  def displayMammalFeatures(self):
    print('Mammal is a warm-blooded animal.')
```

Let's derive a new class  Dog  from this  `Mammal`  class.

```
class Mammal:
  def displayMammalFeatures(self):
    print('Mammal is a warm-blooded animal.')

class Dog(Mammal):
  def displayDogFeatures(self):
    print('Dog has 4 legs.')

d = Dog()
d.displayDogFeatures()
d.displayMammalFeatures()
```

Run Code

Notice that we are able to call method of base class  `displayMammalFeatures()`  from the object of derived class  d.

To learn more about inheritance and method overriding, visit  [Python Inheritance](https://www.programiz.com/python-programming/inheritance).

We also suggest you to check  [multiple inheritance](https://www.programiz.com/python-programming/multiple-inheritance)  and  [operator overloading](https://www.programiz.com/python-programming/operator-overloading)  if you are interested.

----------

## Miscellaneous and Advance Topics

----------

### Iterators

Iterator in Python is simply an object that can be iterated upon. An object which will return data, one element at a time.

Technically speaking, Python iterator object must implement two special methods,  `__iter__()`  and  `__next__()`, collectively called the iterator protocol.

An object is called iterable if we can get an iterator from it. Most of built-in containers in Python like: list, tuple, string etc. are iterables.

The  `iter()`  function (which in turn calls the  `__iter__()`  method) returns an iterator from them.

```
my_list = [4, 7, 0, 3]

# get an iterator using iter()
my_iter = iter(my_list)

print(next(my_iter)) # Output: 4
print(next(my_iter)) # Output: 7
```

Run Code

To learn more about infinite iterators and how to create custom iterators, visit:  [Python Iterators](https://www.programiz.com/python-programming/iterator).

----------

### Generators

There is a lot of overhead in building an iterator in Python; we have to implement a class with  `__iter__()`  and  `__next__()`  method, keep track of internal states, raise  `StopIteration`  when there was no values to be returned etc.

This is both lengthy and counter intuitive. Generator comes into rescue in such situations.

Python generators are a simple way of creating iterators.

Learn more about  [Python Generators](https://www.programiz.com/python-programming/generator).

----------

### Closures

This technique by which some data gets attached to the code is called closure in Python.

```
def print_msg(msg): # outer enclosing function
    def printer():  # inner function
        print(msg)
    return printer  # this got changed

another = print_msg("Hello") # Output: Hello
another()
```

Run Code

Here, the  `print_msg()`  function is called with the string  `"Hello"`  as an argument and the returned function was bound to the name  another. On calling  `another()`, the message was still remembered although we had already finished executing the  `print_msg()`  function.

The criteria that must be met to create closure in Python are summarized in the following points.

-   We must have a nested function (function inside a function).
-   The nested function must refer to a value defined in the enclosing function.
-   The enclosing function must return the nested function.

Visit  [Python closures](https://www.programiz.com/python-programming/closure)  to learn more about closures and when to use them.