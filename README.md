# Python Beginner's Cheat Sheet

## Table of Contents
1. [Basics](#basics)
2. [Data Types](#data-types)
3. [Variables](#variables)
4. [Operators](#operators)
5. [Mathematical Calculations](#mathematical-calculations)
6. [Control Flow](#control-flow)
7. [Functions](#functions)
8. [Collections](#collections)
## Bits of Coding Practice
9. []()

---

## Basics
```python
# Print statement
print("Hello, World!")

# Comments
# This is a single-line comment

"""
This is a
multi-line comment
"""

# Indentation
if 5 > 2:
    print("Five is greater than two!")

# F Strings
score = 1.697546
print(f"Your score is {score}")

# F Strings with decimal places
print(f"Each person should pay: ${final_amount:.2f}")

```

## Data Types
```python
# Integer
x = 5

# Float
y = 3.14

# String
name = "Alice"

# Boolean
is_valid = True

# NoneType
nothing = None

```

## Variables
```python
# Variable assignment
a = 10
b = 20

# Multiple assignment
x, y, z = 1, 2, 3

```

## Operators
```python
# Arithmetic Operators
add = 5 + 2
sub = 5 - 2
mul = 5 * 2
div = 5 / 2
mod = 5 % 2
exp = 5 ** 2
floor_div = 5 // 2

# Comparison Operators
equal = (5 == 2)
not_equal = (5 != 2)
greater = (5 > 2)
less = (5 < 2)
greater_equal = (5 >= 2)
less_equal = (5 <= 2)

# Logical Operators
and_op = (5 > 2 and 5 < 10)
or_op = (5 > 2 or 5 < 2)
not_op = not (5 > 2)

```

## Mathematical Calculations
```python
# Absolute Value: abs()
result = abs(-5)  # result is 5

# Round: round()
result = round(3.6)  # result is 4

# Ceiling: math.ceil()
import math
result = math.ceil(3.2)  # result is 4

# Floor: math.floor()
import math
result = math.floor(3.8)  # result is 3

# Square Root: math.sqrt()
import math
result = math.sqrt(16)  # result is 4.0

# Power: pow()
result = pow(2, 3)  # result is 8

# Maximum: max()
result = max(1, 5, 3)  # result is 5

# Minimum: min()
result = min(1, 5, 3)  # result is 1

# Sum: sum()
result = sum([1, 2, 3, 4])  # result is 10

```

## Control Flow
```python
# If-Else Statements
if x > 0:
    print("x is positive")
elif x == 0:
    print("x is zero")
else:
    print("x is negative")

# For Loop
for i in range(5):
    print(i)

# While Loop
count = 0
while count < 5:
    print(count)
    count += 1

```

## Functions
```python
# Function definition
def greet(name):
    return f"Hello, {name}!"

# Function call
print(greet("Alice"))

```

## Collections

### Lists

- Ordered: The items in a list have a defined order, and this order will not change unless explicitly changed by methods like sort().
- Indexed: Items in a list can be accessed by their position (index).
- Mutable: Lists can be changed after their creation. Items can be added, removed, or changed.
- Allows Duplicates: Lists can contain multiple occurrences of the same item.

#### Creating Lists
```python
# Empty list
empty_list = []

# List with elements
fruits = ["apple", "banana", "cherry"]

# List with mixed data types
mixed_list = [1, "hello", 3.14, True]

```

#### Accessing Elements
```python
# Accessing elements by index (0-based)
first_fruit = fruits[0]  # "apple"
last_fruit = fruits[-1]  # "cherry"

```

#### Slicing lists
```python
# Slicing syntax
my_list[ start : stop : step ]

# Ommitting Sections
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers[:3] # Gives [0, 1, 2]
numbers[3:] # Gives [3, 4, 5, 6, 7, 8, 9]

# Using Only the "Step" Section
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers[::2] # Gives [0, 2, 4, 6, 8]

# Negative Indices
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
numbers[-3:] # Gives [7, 8, 9]

```

#### Modifying Lists
```python
# Changing an element
fruits[1] = "blueberry"  # ["apple", "blueberry", "cherry"]

# Adding elements
fruits.append("orange")  # ["apple", "blueberry", "cherry", "orange"]
fruits.insert(1, "banana")  # ["apple", "banana", "blueberry", "cherry", "orange"]

# Removing elements
fruits.remove("banana")  # ["apple", "blueberry", "cherry", "orange"]
popped_fruit = fruits.pop()  # "orange", ["apple", "blueberry", "cherry"]
del fruits[1]  # ["apple", "cherry"]

```

#### List Operations
```python
# Length of a list
length = len(fruits)  # 2

# Concatenating lists
more_fruits = fruits + ["mango", "pineapple"]  # ["apple", "cherry", "mango", "pineapple"]

# Repeating lists
repeated_fruits = fruits * 2  # ["apple", "cherry", "apple", "cherry"]

```

#### List Methods
```python
# Count occurrences of an element
count_cherries = fruits.count("cherry")  # 1

# Find index of an element
index_apple = fruits.index("apple")  # 0

# Reverse the list
fruits.reverse()  # ["cherry", "apple"]

# Sort the list
fruits.sort()  # ["apple", "cherry"]

```

#### Iterating Through Lists
```python
# Using a for loop
for fruit in fruits:
    print(fruit)

# Using list comprehensions
uppercase_fruits = [fruit.upper() for fruit in fruits]  # ["APPLE", "CHERRY"]

```

#### Copying Lists
```python
# Shallow copy
copy_fruits = fruits.copy()

# Using slicing
copy_fruits = fruits[:]

# Using the list() function
copy_fruits = list(fruits)

```

#### Important List Functions
```python
# Checking membership
is_apple_in_list = "apple" in fruits  # True
is_mango_in_list = "mango" not in fruits  # True

# Finding the maximum and minimum
numbers = [10, 20, 30, 40, 50]
max_num = max(numbers)  # 50
min_num = min(numbers)  # 10

# Summing elements
total = sum(numbers)  # 150

```

### Dictonaries

- Key-Value Pairs: Dictionaries store data in key-value pairs. Each key is unique and maps to a value.
- Unordered (until Python 3.7): The items are not stored in a specific order. (Note: As of Python 3.7, dictionaries maintain insertion order, but this is considered an implementation detail.)
- Mutable: You can change, add, or remove key-value pairs after the dictionary is created.
- No Duplicate Keys: Each key must be unique, but values can be duplicated.

#### Creating a Dictionary
```python
# Empty dictionary
my_dict = {}

# Dictionary with initial values
my_dict = {
    'key1': 'value1',
    'key2': 'value2',
    'key3': 'value3'
}

```
#### Accessing Values
```python
# Accessing a value by key
value = my_dict['key1']  # returns 'value1'

# Using the `get` method (returns None if the key doesn't exist)
value = my_dict.get('key2')  # returns 'value2'
value = my_dict.get('nonexistent_key')  # returns None

# Using a default value with `get`
value = my_dict.get('nonexistent_key', 'default_value')  # returns 'default_value'

```
#### Adding or Updating Values
```python
# Adding a new key-value pair
my_dict['new_key'] = 'new_value'

# Updating an existing key-value pair
my_dict['key1'] = 'updated_value1'

```
#### Removing Key-Value Pairs
```python
# Using `del` to remove a key-value pair
del my_dict['key1']

# Using the `pop` method (returns the removed value)
value = my_dict.pop('key2')  # returns 'value2'

# Removing and returning an arbitrary key-value pair (Python 3.7+)
key, value = my_dict.popitem()  # returns a tuple (key, value)

```
#### Checking for Keys
```python
# Check if a key exists in the dictionary
exists = 'key1' in my_dict  # returns True or False

# Check if a key does not exist in the dictionary
not_exists = 'nonexistent_key' not in my_dict  # returns True or False

```
#### Iterating Over Dictionaries
```python
# Iterating over keys
for key in my_dict:
    print(key)

# Iterating over values
for value in my_dict.values():
    print(value)

# Iterating over key-value pairs
for key, value in my_dict.items():
    print(f'Key: {key}, Value: {value}')

```
#### Merging Dictionaries
```python
# Using the `update` method
dict1 = {'a': 1, 'b': 2}
dict2 = {'b': 3, 'c': 4}
dict1.update(dict2)  # dict1 is now {'a': 1, 'b': 3, 'c': 4}

# Using the `**` operator (Python 3.5+)
dict1 = {**dict1, **dict2}  # dict1 is now {'a': 1, 'b': 3, 'c': 4}

```

### Sets

- Unordered: Sets do not maintain any order of elements.
- Unindexed: You cannot access items in a set by referring to an index.
- Mutable: You can add or remove items, but you cannot change an existing item (although the set itself is mutable).
- No Duplicates: Sets do not allow duplicate items. Each item must be unique.

#### Basics
```python
# Sets are like Lists, but they are unordered and they guarantee uniqueness. Only ONE of each value can be in a set.
fruits = {'apple', 'banana', 'grape'}
print(type(fruits))
# Prints: <class 'set'>

print(fruits)
# Prints: {'banana', 'grape', 'apple'}

```

#### Add Values
```python
fruits = {'apple', 'banana', 'grape'}
fruits.add('pear')
print(fruits)
# Prints: {'banana', 'grape', 'pear', 'apple'}
```

#### Empty Set
```python
# Because the empty bracket {} syntax creates an empty dictionary, to create an empty set, you need to use the set() function.

fruits = set()
fruits.add('pear')
print(fruits)
# Prints: {'pear'}

```

#### Iterating Over Values in a Set
```python
fruits = {'apple', 'banana', 'grape'}
for fruit in fruits:
    print(fruit)
    # Prints:
    # banana
    # grape
    # apple

```

#### Removeing Values
```python
fruits = {'apple', 'banana', 'grape'}
fruits.remove('apple')
print(fruits)
# Prints: {'banana', 'grape'}

```

#### Topic
```python

```
#### Topic
```python

```

## Bits of Coding Practice
### Life in Weeks
```python
age = input()

total_weeks_90 = 90 * 52
your_weeks = int(age) * 52
weeks_left = total_weeks_90 - your_weeks

print(f"You have {weeks_left} weeks left.")
```

### Odd or Even
```python
number = int(input())

if number % 2 == 0:
  print("This is an even number.")
else:
  print("This is an odd number.")
```

## Title
```python

```
