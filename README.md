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
# Output = 5000
```

## Strings
```python
# A string is a series of characters inside of quotes
my_string = "This is a string!"
print(my_string)
# Output = This is a string!

# You can change the case in strings with methods
name = 'rachael pracht'
print(f"This is the original string: {name}")
print(f"This is the string with title case added: {name.title()}")
# Output = This is the original string: rachael pracht
# Output = This is the string with title case added: Rachael Pracht


# You can also change the case to all UPPER case or all lower case
new_string = "Here Is My Example"
print(new_string.upper())
print(new_string.lower())
# Output = HERE IS MY EXAMPLE
# Output = here is my example

# You can add a tab to your text
no_tab = "Python"
add_tab = "\tPython"
print(no_tab)
print(add_tab)
# Output = Python
# Output =     Python

# You can add a new line to your text
add_line = "This text\nhas a new line"
print(add_line)
# Output =
# This text
# has a new line

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
# Output = https://google.com
# Output = google.com

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

### Creating a List & Accessing Elements
```python
items = []

bicycles = ['trek', 'cannondale', 'redline', 'salsa', 'specialized']
print(bicycles)
# Output = ['trek', 'cannondale', 'redline', 'salsa', 'specialized']

# You access list items by utilizing the index, which looks like bicycles[0]
# Output: trek
print(bicycles[0])

# You can use string methods in lists
print(bicycles[0].title())
# Output: Trek

# To find the last item of a list
print(bicycles[-1])
# Output: specialized

# Using Individual Elements from Lists
message = f"My first bicycle was a {bicycles[0].title()}."
print(message)
# Output = My first bicycle was a Trek.
```
### Modifying, Adding, and Inserting Elements
```python
# Modifying Elements
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)
# Output = ['honda', 'yamaha', 'suzuki']

motorcycles[0] = "ducati"
print(motorcycles)
Output = ['ducati', 'yamaha', 'suzuki']

# Adding Elements
motorcycles.append("honda")
print(motorcycles)
# Output = ['ducati', 'yamaha', 'suzuki', 'honda']

# Adding Elements Using Inputs
groceries = []
groceries.append(input("Add grocery item: "))
print(groceries)

# Inserting Elements into a List
motorcycles = ['ducati', 'yamaha', 'suzuki', 'honda']
motorcycles.insert(0, 'harley')
print(motorcycles)
# Output = ['harley', 'ducati', 'yamaha', 'suzuki', 'honda']
```
### Removing Elements from a List
```python
# Using the del Statment
motorcycles = ['harley', 'ducati', 'yamaha', 'suzuki', 'honda']
del motorcycles[0]
print(motorcycles)
# Output = ['ducati', 'yamaha', 'suzuki', 'honda']

# Using the pop() Method
motorcycles = ['harley', 'ducati', 'yamaha', 'suzuki', 'honda']
popped_motorcycle = motorcycles.pop()
print(motorcycles)
# Output = ['harley', 'ducati', 'yamaha', 'suzuki']
print(popped_motorcycle)
# Output = honda

# Using the pop() method from Any Position in List
motorcycles = ['harley', 'ducati', 'yamaha', 'suzuki', 'honda']
first_owned = motorcycles.pop(0)
print(f"The first motorcycle I owned was a {first_owned.title()}.")
# Output = The first motorcycle I owned was a Harley.

# Removing an Item by Value
motorcycles = ['ducati', 'yamaha', 'suzuki', 'honda']
print(motorcycles)
# Output = ['ducati', 'yamaha', 'suzuki', 'honda']

motorcycles.remove('ducati')
print(motorcycles)
# Output = ['yamaha', 'suzuki', 'honda']
```
### Organizing a List
```python
# Sorting a List Permanently with sort() Method
cars = ['bmw', 'audi', 'toyota', 'subaru']
print(cars)
# Output = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort()
print(cars)
# Output = ['audi', 'bmw', 'subaru', 'toyota']

# Sorting in reverse
cars.sort(reverse=True)
print(cars)
# Output = ['toyota', 'subaru', 'bmw', 'audi']

# Sorting a List Temporarily with the sorted() Function
cars = ['bmw', 'audi', 'toyota', 'subaru']

print("Here is the original list:")
print(cars)

print("Here is the sorted list:")
print(sorted(cars))

print("Here is the original list again:")
print(cars)

# Printing a List in Reverse Order (not reversed SORTED order)
# (This is just the list printed BACKWARDS)
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.reverse()
print(cars)
# Output = ['subaru', 'toyota', 'audi', 'bmw']

# Finding the Length of a List
cars = ['bmw', 'audi', 'toyota', 'subaru']

print(len(cars))
# Output = 4
```
### Working With Lists
```python

```
