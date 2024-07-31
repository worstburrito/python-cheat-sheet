# Python Beginner's Cheat Sheet

## Table of Contents
1. [Variables](#variables)
2. [Strings](#strings)
3. [Numbers](#numbers)
4. [Lists](#lists)


---

## Variables
```python
# Variables are labels you can assign and reassign values to
message = "Python is so awesome to learn!"
print(message)
# Output: Python is so awesome to learn!

# If you reassign a variable and print it again, it will change
message = "I love learning Python!"
print(message)
# Output: I love learning Python!

# You can assign multiple vars on the same line
x, y, z = 1, 2, 3

# Variables have rules, such as:
# They can only contain letters, numbers and underscores
# They cannot start with numbers
# Spaces are not allowed, you use underscores instead
# Avoid using words that Python uses for operations and functions
# Examples:
# message_1, my_message

# Constants
# Python doesn't have built-in const
# Programmers use ALL CAPS vars to represent
NEVER_CHANGES = 5000
print(NEVER_CHANGES)
```

## Strings
```python
# A string is a series of characters inside of quotes
my_string = "This is a string!"
print(my_string)

# You can change the case in strings with methods
name = 'rachael pracht'
print(f"This is the original string: {name}")
print(f"This is the string with title case added: {name.title()}")

# You can also change the case to all UPPER case or all lower case
new_string = "Here Is My Example"
print(new_string.upper())
print(new_string.lower())

# You can add a tab to your text
no_tab = "Python"
add_tab = "\tPython"
print(no_tab)
print(add_tab)

# You can add a new line to your text
add_line = "This text\nhas a new line"
print(add_line)

# You can strip spaces from strings
enter_msg = input("Enter a string: ").strip()
print(enter_msg)

# .lstrip() removes spaces from the left
# .rstrip() removes space from the right

# Removing Prefixes
a_url = "https://google.com"
new_url = a_url.removeprefix("https://")
print(a_url)
print(new_url)

```

## Numbers
```python
# Integers
# You can +, -, *, / integers
result = 2 + 3
print(result)
result = 2 * 3
print(result)
result = 9 - 3
print(result)
result = 9 / 3
print(result)

# Exponents **
result = 3 ** 3
print(result)

# Floats
# Numbers with decimal points
result = 2.5 * 2
print(result)

# Underscores in Numbers instead of commas
# Makes large numbers easier to read
one_mil = 1_000_000
print(one_mil)

```

## Lists

- Ordered: The items in a list have a defined order, and this order will not change unless explicitly changed by methods like sort().
- Indexed: Items in a list can be accessed by their position (index).
- Mutable: Lists can be changed after their creation. Items can be added, removed, or changed.
- Allows Duplicates: Lists can contain multiple occurrences of the same item.

### Creating Lists
```python
# Empty list
empty_list = []

# List with elements
fruits = ["apple", "banana", "cherry"]

# List with mixed data types
mixed_list = [1, "hello", 3.14, True]

```

### Accessing Items
```python
# Accessing elements by index (0-based)
first_fruit = fruits[0]  # "apple"
last_fruit = fruits[-1]  # "cherry"

```

### Slicing Lists
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

### Modifying Lists
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

### List Operations
```python
# Length of a list
length = len(fruits)  # 2

# Concatenating lists
more_fruits = fruits + ["mango", "pineapple"]  # ["apple", "cherry", "mango", "pineapple"]

# Repeating lists
repeated_fruits = fruits * 2  # ["apple", "cherry", "apple", "cherry"]

```

### List Methods
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

### Iterating Through Lists
```python
# Using a for loop
for fruit in fruits:
    print(fruit)

# Using list comprehensions
uppercase_fruits = [fruit.upper() for fruit in fruits]  # ["APPLE", "CHERRY"]

```

### Copying Lists
```python
# Shallow copy
copy_fruits = fruits.copy()

# Using slicing
copy_fruits = fruits[:]

# Using the list() function
copy_fruits = list(fruits)

```

### Important List Functions
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

### Nested Lists
```python
# Nesting Lists in Lists
# dirty_dozen = ["Strawberries", "Spinach", "Kale", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears", "Tomatoes", "Celery", "Potatoes"]

fruits = ["Strawberries", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears"] 
vegetables = ["Spinach", "Kale", "Tomatoes", "Celery", "Potatoes"]

dirty_dozen = [fruits, vegetables]

print(dirty_dozen)
# [['Strawberries', 'Nectarines', 'Apples', 'Grapes', 'Peaches', 'Cherries', 'Pears'], ['Spinach', 'Kale', 'Tomatoes', 'Celery', 'Potatoes']]

# Nesting Dictionaries in Lists
travel_log = [
    {
        "country": "France",
        "cities_visited": ["Paris", "Lille", "Dijon"],
        "total_visits": 12
    },
    {
        "country": "Germany",
        "cities_visited": ["Berlin", "Hamburg", "Stuttgart"],
        "total_visits": 5
    }, 
]
```

