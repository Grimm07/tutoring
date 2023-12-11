# Basic Python Coding Tutorial

## Introduction
Welcome to this Python tutorial! Python is a high-level, interpreted programming language known for its readability and versatility. It's ideal for beginners due to its simple syntax and also powerful enough for advanced programming tasks. It's widely used in fields such as web development, data science, machine learning, and automation.

## Setting Up Your Environment
Before we start coding, you need to set up your Python environment:

1. **Download and Install Python**: Visit [python.org](https://www.python.org/) and download the latest version of Python. Follow the installation instructions for your operating system.
2. **Choose an Editor**: You can use a text editor like Notepad++, or an Integrated Development Environment (IDE) like PyCharm or Visual Studio Code for writing your Python code.

## Basic Syntax
Python's syntax is clear and intuitive. Here are some basic concepts:

- **Tabs**: Python is called a "Tab delimited" language. This means that for your code to run, it should have correct tabbing.
- **Variables**: Variables are used to store information that can be referenced and manipulated. For example: `x = 5`
- **Comments**: Use `#` for commenting. Comments are not executed by Python.
- **Printing Output**: Use the `print()` function to output data. For example: `print("Hello, World!")`

# Data Structures in Python

Python includes several built-in data structures that are used to store collections of data in various formats. Here's an overview of the most commonly used data structures:

## List
A list is a mutable, ordered sequence of elements. Each element can be of a different type.

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")  # Adding an element
print(fruits[0])         # Accessing the first element
```

## Tuple
A tuple is an immutable, ordered sequence of elements. Similar to a list, but you can't change its elements after it's defined.

```python
dimensions = (200, 50)
print(dimensions[0])     # Accessing the first element
```

## Set
A set is an unordered collection with no duplicate elements. Sets are mutable and great for membership testing.
```python
unique_numbers = {1, 2, 3, 3, 4}
print(unique_numbers)    # Output will be {1, 2, 3, 4}
```

## Dictionary
A dictionary is a mutable, unordered collection of key-value pairs. It allows for fast retrieval based on the key.
```python
person = {"name": "Alice", "age": 25}
print(person["name"])    # Accessing the value associated with the key 'name'
```




## Control Structures
Control structures help you control the flow of your program.

- **If Statements**: Used for decision-making operations.
  ```python
  if x > 10:
      print("x is greater than 10")
    ```

- **Loops**: Repeat a block of code
  * For Loop:
    ```python
    for i in range(5):
            print(i)
    ```
  * While Loop: 
    ```python
    i = 0
    while i < 5:
        print(i)
        i += 1
    ```
    **NOTE:** In other languages, it is more common to see `i++` instead of `i+=1` - they mean the same exact thing, one is simply in **postfix** notation
- **Functions**: Functions are blocks of code that perform a specific task and can be reused
    ```python
    def greet(name):
        print("Hello, " + name + "!")
    ```
- **Lambdas**: This is a more complicated version of a function. This is short hand.
    ```python
    myFunc = lambda name: print("Hello, " + name + "!")
    ```

# String Formatting in Python

String formatting in Python allows you to interpolate variables into strings, making it easier to create dynamic and formatted text output. There are several methods to format strings in Python:

## Using the `%` Operator
The `%` operator is an older method for formatting but still used in some codes.
```python
name = "Alice"
greeting = "Hello, %s!" % name
print(greeting)
```

## Using .format()
The format() method introduced in Python 3 is more powerful and flexible. It replaces {} placeholders with the arguments provided in format().
```python
name = "Bob"
age = 25
greeting = "Hello, {}. You are {} years old.".format(name, age)
print(greeting)
```

## F-Strings (Formatted String Literals)
Introduced in Python 3.6, f-strings offer a concise and readable way to embed expressions inside string literals, using curly braces {}.

```python
name = "Carol"
age = 30
greeting = f"Hello, {name}. You are {age} years old."
print(greeting)
```

# Opening Files in Python

Python provides built-in functions to read and write files. Opening a file is typically the first step in file handling. Here's how you can do it:

## Using `open()`
The `open()` function is used to open a file in Python. It takes two main arguments: the file path and the mode.

```python
# Open a file for reading ('r')
file = open('example.txt', 'r')
content = file.read()
file.close()

# Open a file for writing ('w')
file = open('example.txt', 'w')
file.write('Hello, Python!')
file.close()
```

## Using with Statement
It's recommended to use the with statement when dealing with file objects. This ensures that the file is properly closed after its suite finishes, even if an exception is raised.
```python
# Reading a file
with open('example.txt', 'r') as file:
    content = file.read()

# Writing to a file
with open('example.txt', 'w') as file:
    file.write('Hello, Python!')

```
* **NOTE** Remember, when opening a file in 'w' mode, the file is truncated (i.e., all existing file content is deleted), and if the file doesn't exist, Python will create it for you.

# Import Statements in Python

Import statements in Python are used to bring in modules (libraries or collections of code) that provide additional functionality. This allows for more modular and organized code. Here's how they work:

## Using `import`
The `import` statement is used to import an entire module. You can then access its functions, classes, and attributes using the module name followed by a dot.

```python
import math
print(math.sqrt(16))  # Accessing the square root function from the math module
```

## Using `from ... import ...`
If you only need specific functions or classes from a module, you can use `from ... import ...` to import only those.
```python
from math import sqrt
print(sqrt(16))  # Directly using the sqrt function without the module name prefix
```

## Importing with Aliases
Sometimes, for convenience or to avoid naming conflicts, you might want to import a module or function under a different name. This can be done using as.
```python
import math as m
print(m.sqrt(16))  # Using an alias for the math module
```

## Importing Everything (Not Recommended)
You can import everything from a module using *, but this is generally discouraged as it can lead to unclear code and naming conflicts.
```python
from math import *
print(sqrt(16))  # Every function and class from math is now available directly
```