# Python Beginner's Cheat Sheet

## Table of Contents
1. [Variables](#variables)
2. [Strings](#strings)
3. [Numbers](#numbers)
4. [Lists](#lists)
5. [List Methods](#list-methods)
6. [Tuples](#tuples)
7. [If Statements](#if-statements)
8. [Dictonaries](#dictionaries)
9. [Dictionary Methods](#dictionary-methods)
10. [Nesting](#nesting)
11. [User Input & While Loops](#user-input--while-loops)
12. [Functions](#functions)
13. [Classes](#classes)


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
- [Creating a List & Accessing Elements](#creating-a-list--accessing-elements)
- [Modifying, Adding, and Inserting Elements](#modifying-adding-and-inserting-elements)
- [Removing Elements from a List](#removing-elements-from-a-list)
- [Organizing a List](#organizing-a-list)
- [Working With Lists](#organizing-a-list)
- [Working With Parts of Lists](#working-with-parts-of-lists)

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
# Looping Through an Entire List
fruits = ['apple','banana','cherry','pear','strawberry','orange']
for fruit in fruits:
    print(fruit)
# Output = will list each fruit on an individual line

# Using the range() function
for value in range(1, 5):
    print(value)
# Output = will list 1-4 on individual lines
# You can also pass one agrument
for value in range(6):
    print(value)
# Output = will start at 0 and end at 5

# Using range() to make a list of numbers
even_nums = list(range(2,11,2))
print(even_nums)
# Output = [2, 4, 6, 8, 10]

# List of Square Nums example
squares = []
for value in range(1,11):
    squares.append(value**2)
print(squares)
# Output = [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# Simple Statistics with a List of Nums
digits = [1,2,3,4,5,6,7,8,9,0]
print(min(digits))      # Output = 0
print(max(digits))      # Output = 9
print(sum(digits))      # Output = 45

# List Comprehensions
squares = [value**2 for value in range(1,11)]
print(squares)
# Output = [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

# The code above does the same as
squares = []
for value in range(1,11):
    squares.append(value**2)
print(squares)
# Output = [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
### Working With Parts of Lists
```python
# Slicing a List
fruits = ['apple','banana','cherry','pear','strawberry','orange']
print(fruits[:3])
# Output = ['apple', 'banana', 'cherry']

# You only need a starting index if you want
# To slice anything after index 0
# Same for end, it will just go to the last element
print(fruits[2:5])
# Output = ['cherry', 'pear', 'strawberry']
print(fruits[2:])
# Output = ['cherry', 'pear', 'strawberry', 'orange']

# A third value will 'step' similar to range functions
print(fruits[::2])
# Output = ['apple', 'cherry', 'strawberry']

# Looping Through a Slice
fruits = ['apple','banana','cherry','pear','strawberry','orange']
print("Here are the last 3 fruits on my list:")
for fruit in fruits[-3::]:
    print(fruit)
# Output = Here are the last 3 fruits on my list:
# pear
# strawberry
# orange

# Copying a List
fruits = ['apple','banana','cherry','pear','strawberry','orange']
favorite_fruits = fruits[:]
print(favorite_fruits)
# Output = ['apple', 'banana', 'cherry', 'pear', 'strawberry', 'orange']

favorite_fruits.remove('apple')
favorite_fruits.remove('pear')
favorite_fruits.append('watermelon')
print(favorite_fruits)
# Output = ['banana', 'cherry', 'strawberry', 'orange', 'watermelon']
```

## List Methods
```python
# Used for adding elements to the end of the List. 
append()
# Syntax: list.append(element)

# It returns a shallow copy of a list
copy()

# This method is used for removing all items from the list.
clear()

# These methods count the elements.
count()
# Syntax: List.count(element)

# Adds each element of an iterable to the end of the List
extend()
# Syntax: List1.extend(List2)

# Returns the index of the first occurrence. The start and end indexes are not necessary parameters. 
index()
# Syntax: List.index(element[,start[,end]])

# Inserts a given element at a given index in a list.
insert()
# Syntax: list.insert(position, element)

# Removes and returns the last value from the List or the given index value.
pop()
# Syntax: list.pop([index])

# Removes a given object from the List.
remove()
# Syntax: list.remove(element)

# Deletes an element from the list using it’s index.
del
# Syntax: del list.[index]

# Reverses objects of the List in place.
reverse()
# Syntax: list. reverse()

# Sort a List in ascending, descending, or user-defined order
sort()
# Syntax: list.sort([key,[Reverse_flag]])

# Calculates the minimum of all the elements of the List
min()
# Syntax: min(iterable, *iterables[, key])

# Calculates the maximum of all the elements of the List
max()
# Syntax: max(iterable, *iterables[, key])

# Calculates the sum of all the elements of the List
sum()
# Syntax: sum(List)

# Calculates the total length of the List.
len()
# Syntax: len(list_name)

# Returns a sequence of numbers, in a given range
range()
# Syntax: range(start, stop, step)
```
## Tuples
```python
# Defining a Tuple
# Tuple are good for storing values that should
# not change.
dimensions = (200,50)
print(dimensions[0])
# Output = 200
print(dimensions[1])
# Output = 50

# Looping Through all Values in a Tuple
for dimension in dimensions:
    print(dimension)
# Output = 200
# 50

# Writing Over a Tuple
dimensions = (200,50)
print("Original dimensions:")
for dimension in dimensions:
    print(dimension)
# Output = Original dimensions:
# 200
# 50

dimensions = (400,100)
print("\nModified dimensions:")
for dimension in dimensions:
    print(dimension)
# Output = Modified dimensions:
# 400
# 100
```
## If Statements
- [Comparisons](#comparisons)
- [Simple If Statements](#simple-if-statements)
- [Using if Statements with Lists](#using-if-statements-with-lists)
### Comparisons
```python
# A Simple Example
cars = ['audi', 'bmw', 'subaru', 'toyota']
for car in cars:
    if car == 'bmw':
        print(car.upper())
    else:
        print(car.title())

# Output = Audi
# BMW
# Subaru
# Toyota

# A note: '=' is an assignment while '==' is a comparison
car = 'Audi'
print(car == 'Audi')
# Output = True
print(car == 'BMW')
# Output = False

# Comparisons are case-sensitive
car = 'Audi'
print(car == 'audi')
# Output = False
print(car.lower() == 'audi')
# Output = True

# Checking for Inequality using !=
requested_topping = 'mushrooms'
if requested_topping != 'anchovies':
    print("Hold the anchovies!")
# Output = Hold the anchovies!

# Mathematical Comparisons
age = 18
print(age < 21)
# Output = True
print(age > 21)
# Output = False
print(age <= 21)
# Output = True
print(age >= 21)
# Output = False
print(age != 21)
# Output = True

# Using 'and' to check Multiple Conditions
age1 = 22
age2 = 18
print((age1 >= 21) and (age2 >= 21))
# Output = False
age2 = 22
print((age1 >= 21) and (age2 >= 21))
# Output = True

# Using 'or' to check Multiple Conditions
age1 = 22
age2 = 18
print((age1 >= 21) or (age2 >= 21))
# Output = True
age1 = 18
print((age1 >= 21) or (age2 >= 21))
# Output = False

# Checking if a Value is or is NOT in a list
requested_toppings = ['mushrooms', 'onions', 'pineapple']
print('mushrooms' in requested_toppings)
# Output = True
print('pepperoni' in requested_toppings)
# Output = False

banned_users = ['susan', 'chad', 'stacy']
user = 'marie'
if user not in banned_users:
    print(f"{user.title()}, you can post a response if you wish!")
# Output = Marie, you can post a response if you wish!
```
### Simple If Statements
```python
# Simple if Statements
age = 19
if age >= 18:
    print("You can vote!")
# Output = You can vote!

# if-else Statements
age = 17
if age >= 18:
    print("You can vote!")
else:
    print("You cannot vote.")
# Output = You cannot vote.

# if-elif-else Statements
age = int(input("Enter your age: "))

if age <= 4:
    cost = 0
elif 4 < age < 18:
    cost = 25
else:
    cost = 40

print(f"Your admission costs: ${cost}")
# Input = 4, Output = Your admission costs: $0
# Input = 12, Output = Your admission costs: $25

# You do not need to include an else block
# if it makes more sense to just use elif
age = int(input("Enter your age: "))

if age < 4:
    cost = 0
elif age < 18:
    cost = 25
elif age < 65:
    cost = 40
elif age >= 65:
    cost = 20

print(f"Your admission costs: ${cost}")
# Input = 3, Output = Your admission costs: $0
# Input = 67, Output = Your admission costs: $20

# Testing Multiple Conditions
requested_toppings = ['mushrooms', 'extra cheese']

if 'mushrooms' in requested_toppings:
    print("Adding mushrooms...")
if 'pepperoni' in requested_toppings:
    print("Adding pepperoni...")
if 'extra cheese' in requested_toppings:
    print("Adding extra cheese...")
print("Your pizza is ready!")
# Output = Adding mushrooms...
# Adding extra cheese...
# Your pizza is ready!

# If you only want one block of code to run, use if-elif-else
# If you want more than one block of code to run, use independent if statements
```
### Using if Statements with Lists
```python
# Checking for Special Items
requested_toppings = ['mushrooms', 'green peppers', 'extra cheese']

for requested_topping in requested_toppings:
    print(f"Adding {requested_topping} to your pizza!")
print("Your pizza is ready.")
# Output = Adding mushrooms to your pizza!
# Adding green peppers to your pizza!
# Adding extra cheese to your pizza!
# Your pizza is ready.

# Using an if Statement in the Above Example
for requested_topping in requested_toppings:
    if requested_topping == 'green peppers':
        print("Sorry, we are out of green peppers.")
    else:
        print(f"Adding {requested_topping} to your pizza!")
print("Your pizza is ready.")
# Output = Adding mushrooms to your pizza!
# Sorry, we are out of green peppers.
# Adding extra cheese to your pizza!
# Your pizza is ready.

# Checking That a List is Not Empty
requested_toppings = []

if requested_toppings:
    for requested_topping in requested_toppings:
        print(f"Adding {requested_topping} to your pizza!")
    print("Finished making your pizza!")
else:
    print("Are you sure you want a plain pizza?")
# Output = Are you sure you want a plain pizza?

# Using Multiple Lists
available_toppings = ['mushrooms', 'olives', 'green peppers',
                      'extra cheese', 'pepperoni', 'pineapple']

requested_toppings = ['mushrooms', 'french fries', 'green peppers',]

for requested_topping in requested_toppings:
    if requested_topping in available_toppings:
        print(f"Adding {requested_topping} to your pizza!")
    else:
        print(f"Sorry, we don't have {requested_topping}.")

print("Finished making your pizza!")
# Output = Adding mushrooms to your pizza!
# Sorry, we don't have french fries.
# Adding green peppers to your pizza!
# Finished making your pizza!
```
## Dictionaries
- [Working With Dictionaries](working-with-dictionaries)
- [Looping Through Dictionaries](#looping-through-dictionaries)
- [Dictionary Methods](#dictionary-methods)

```python
# A Simple Dictionary
alien1 = {'color': 'green', 'points': 5}
print(alien1['color'])
print(alien1['points'])
# Output = green
# 5
```
### Working With Dictionaries
```python
# Accessing Values in a Dictionary
alien1 = {'color': 'green'}
print(alien1['color'])
# Output = green

alien2 = {'color': 'blue', 'points': 10}
pts_earned = alien2['points']
print(f"You earned {pts_earned} points!")
# Output = You earned 10 points!

# Adding New Key-Value Pairs
alien1 = {'color': 'green', 'points': 5}
print(alien1)
# Output = {'color': 'green', 'points': 5}

alien1['x-position'] = 0
alien1['y-position'] = 25
print(alien1)
# Output = {'color': 'green', 'points': 5, 'x-position': 0, 'y-position': 25}

# Starting with an Empty Dictionary
alien1 = {}

alien1['color'] = 'green'
alien1['points'] = 5
print(alien1)
# Output = {'color': 'green', 'points': 5}

# Modifying Values in a Dictionary
alien1 = {'color': 'green'}
print(f"The alien is {alien1['color']}.")
# Output = The alien is green.

alien1['color'] = 'yellow'
print(f"The alien is now {alien1['color']}.")
# Output = The alien is now yellow.

# A more interesting example of this...
alien_0 = {'x-pos': 0, 'y-pos': 25, 'speed': 'medium'}
print(f"Original position: {alien_0['x-pos']}")

# Move the alien to the right.
# Determine how far to move the alien based on its current speed.
if alien_0['speed'] == 'slow':
    x_incr = 1
elif alien_0['speed'] == 'medium':
    x_incr = 2
else: # This must be a fast alien
    x_incr = 3

# The new position is the position plus the increment
alien_0['x-pos'] = alien_0['x-pos'] + x_incr
print(f"New position: {alien_0['x-pos']}")
# Output = Original position: 0
# New position: 2

# Removing Key-Value Pairs
alien1 = {'color': 'green', 'points': 5}
print(alien1)
# Output = {'color': 'green', 'points': 5}

del alien1['points']
print(alien1)
# Output = {'color': 'green'}

# You can use a dictionary to:
# Store many kinds of information about one object OR
# one kind of information about many objects.

favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',

}

language = favorite_languages['sarah'].title()
print(f"Sarah's favorite language is {language}.")
# Output = Sarah's favorite language is C.

# Using get() to Access Values
alien_0 = {'color': 'green', 'speed': 'slow'}
point_value = alien_0.get('points', 'No point value assigned.')
print(point_value)
# Output = No point value assigned.
```
### Looping Through Dictionaries
```python
# Looping Through All Key-Value Pairs
user_0 = {
    'username': 'worstburrito',
    'first': 'rachael',
    'last': 'pracht',
}

for key, value in user_0.items():
    print(f'{key.title()}: {value.title()}')
# Output = Username: Worstburrito
# First: Rachael
# Last: Pracht

# Another Example
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
}

for name, language in favorite_languages.items():
    print(f"{name.title()}'s favorite language is {language.title()}.")
# Output = Jen's favorite language is Python.
# Sarah's favorite language is C.
# Edward's favorite language is Ruby.
# Phil's favorite language is Python.

# Looping Through All the Keys in a Dictionary
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
}

for name in favorite_languages.keys():
    print(name.title())
# Output = Jen
# Sarah
# Edward
# Phil

friends = ['phil', 'sarah']
for name in favorite_languages.keys():
    print(f"Hi {name.title()}.")

    if name in friends:
        language = favorite_languages[name].title()
        print(f"\t{name.title()}, I see you love {language}.")
# Output = Hi Jen.
# Hi Sarah.
# 	Sarah, I see you love C.
# Hi Edward.
# Hi Phil.
# 	Phil, I see you love Python.

if 'erin' not in favorite_languages.keys():
    print("Erin, please take our poll!")
# Output = Erin, please take our poll!

# Looping Through a Dictionaries Keys in a Particular Order
favorite_languages = {
    'jen': 'python',
    'sarah': 'c',
    'edward': 'ruby',
    'phil': 'python',
}

for name in sorted(favorite_languages.keys()):
    print(f"{name.title()}, thank you for taking the poll.")
# Output = Edward, thank you for taking the poll.
# Jen, thank you for taking the poll.
# Phil, thank you for taking the poll.
# Sarah, thank you for taking the poll.

# Looping Through All Values in a Dictionary
print("The following languages have been mentioned:")
for language in favorite_languages.values():
    print(language.title())
# Output = The following languages have been mentioned:
# Python
# C
# Ruby
# Python

# Using a Set to See Values Without Repetition
print("The following languages have been mentioned:")
for language in set(favorite_languages.values()):
    print(language.title())
# Output = The following languages have been mentioned:
# Ruby
# Python
# C
```
## Dictionary Methods
```python
# Removes all items from the dictionary
clear()
# Syntax: my_dict.clear()

# Returns a shallow copy of the dictionary
copy()

# Creates a dictionary from the given sequence
fromkeys()

# Returns the value for the given key
get()
# Syntax: print(my_dict.get('Name'))

# Return the list with all dictionary keys with values
items()
# Syntax: print(list(my_dict.items())[1][0])

# Returns a view object that displays a list of all the keys in the dictionary in order of insertion
keys()
# Syntax: print(list(my_dict.keys()))

# Returns and removes the element with the given key
pop()
# Syntax: my_dict.pop('Age')

# Returns and removes the key-value pair from the dictionary
popitem()
# Syntax: my_dict.popitem()

# Returns the value of a key if the key is in the dictionary else inserts the key with a value to the dictionary
setdefault()

# Returns a view object containing all dictionary values, which can be accessed and iterated through efficiently
values()
# Syntax: print(list(my_dict.values()))

# Updates the dictionary with the elements from another dictionary or an iterable of key-value pairs. With this method,
# you can include new data or merge it with existing dictionary entries
update()
# Syntax: my_dict1.update(my_dict2)

# Python any() function returns True if any of the elements of a
# given iterable( List, Dictionary, Tuple, set, etc) are True else it returns False.
any()
# Syntax: any(iterable)
```
## Nesting
- You can store multiple dictionaries in a list
- You can store a list or lists in a dictionary
- You can store a dictionary in a dictionary
```python
# A List of Dictionaries
alien_0 = {'color': 'green', 'points': 5}
alien_1 = {'color': 'yellow', 'points': 10}
alien_2 = {'color': 'red', 'points': 15}

aliens = [alien_0, alien_1, alien_2]

for alien in aliens:
    print(alien)
# Output = {'color': 'green', 'points': 5}
# {'color': 'yellow', 'points': 10}
# {'color': 'red', 'points': 15}

# Create a Fleet of 30 Aliens (cool, lol)
# Make an empty list for storing our aliens
aliens = []

# Make 30 green aliens.
for alien_number in range(30):
    new_alien = {'color': 'green', 'points': 5, 'speed': 'slow'}
    aliens.append(new_alien)

# Change the first 3 aliens to a new color and speed
for alien in aliens[:3]:
    if alien['color'] == 'green':
        alien['color'] = 'yellow'
        alien['speed'] = 'medium'
        alien['points'] = 10

# Show the first 5 aliens.
for alien in aliens[:5]:
    print(alien)
print("...")

# Show how many aliens have been created.
print(f"Total number of aliens: {len(aliens)}")

# Output = {'color': 'green', 'points': 5, 'speed': 'slow'}
# {'color': 'green', 'points': 5, 'speed': 'slow'}
# {'color': 'green', 'points': 5, 'speed': 'slow'}
# {'color': 'green', 'points': 5, 'speed': 'slow'}
# {'color': 'green', 'points': 5, 'speed': 'slow'}
# ...
# Total number of aliens: 30

# Output after we change the first 3 aliens to yellow = 
# {'color': 'yellow', 'points': 10, 'speed': 'medium'}
# {'color': 'yellow', 'points': 10, 'speed': 'medium'}
# {'color': 'yellow', 'points': 10, 'speed': 'medium'}
# {'color': 'green', 'points': 5, 'speed': 'slow'}
# {'color': 'green', 'points': 5, 'speed': 'slow'}
# ...
# Total number of aliens: 30

# A List in a Dictionary

# Store information abougt a pizza being ordered.
pizza = {
    'crust': 'thick',
    'toppings': ['sausage', 'mushrooms', 'extra cheese'],
}

# Summarize the order.
print(f"You ordered a {pizza['crust']}-crust pizza "
      "with the following toppings:")

for topping in pizza['toppings']:
    print(f"\t{topping}")
    
# Output = 
# You ordered a thick-crust pizza with the following toppings:
# 	sausage
# 	mushrooms
# 	extra cheese

favorite_languages = {
    'Jen': ['Python', 'Ruby', 'JavaScript'],
    'Sarah': ['C++', 'JavaScript'],
    'Edward': ['Rust', 'Go'],
    'Phil': ['Python', 'Haskell'],
}

for name, languages in favorite_languages.items():
    print(f"\n{name.title()}'s favorite languages are:")
    for language in languages:
        print(f"\t{language.title()}")

# Output = 
# Jen's favorite languages are:
# 	Python
# 	Ruby
# 	Javascript
# 
# Sarah's favorite languages are:
# 	C++
# 	Javascript
# 
# Edward's favorite languages are:
# 	Rust
# 	Go
# 
# Phil's favorite languages are:
# 	Python
# 	Haskell

# A Dictionary in a Dictionary

users = {
    'worstburrito': {
        'first': 'rachael',
        'last': 'pracht',
        'location': 'iowa',
    },
    'philmbuff': {
        'first': 'phil',
        'last': 'pracht',
        'location': 'iowa',
    }
}

for username, user_info in users.items():
    print(f"\nUsername: {username}")
    full_name = f"{user_info['first']} {user_info['last']}"
    location = user_info['location']

    print(f"\tFull name: {full_name.title()}")
    print(f"\tLocation: {location.title()}")

# Output =
# Username: worstburrito
# 	Full name: Rachael Pracht
# 	Location: Iowa
# 
# Username: philmbuff
# 	Full name: Phil Pracht
# 	Location: Iowa

```
## User Input & While Loops
- [User Input](#user-input)
- [While Loops](#while-loops)
- [Using a while Loop with Lists and Dictionaries](#using-a-while-loop-with-lists-and-dictionaries)
### User Input
```python
# How the input() Function Works
message = input("Tell me something, and I will repeat it back to you: ")
print(message)
# Output = Pancakes are awesome!

# Writing Clear Prompts
name = input("Please enter your name: ")
print(f"Hello {name}!")

prompt = "If you share your name, we can personalize the messages you see."
prompt += "\nWhat is your first name? "

name = input(prompt)
print(f"Hello {name}!")

# Using int() to Accept a Numeral Input
age = int(input("How old are you? "))
if age < 21:
    print("You are not old enough to drink.")
else:
    print("You are old enough to drink.")

# The Modulo Operator
age = int(input("How old are you? "))
if age % 2 == 0:
    print("Your age is even.")
else:
    print("Your age is odd.")

# Odd or Even Number
number = int(input("Enter a number and I'll tell you if it's odd or even: "))
if number % 2 == 0:
    message = f"{number} is an even number."
else:
    message = f"{number} is an odd number."
print(message)
```
### While Loops
```python
# The while Loop in Action
current_num = 1
while current_num <= 5:
    print(current_num)
    current_num += 1
# Output = 1
# 2
# 3
# 4
# 5

# Letting the User Choose When to Quit
prompt = "\nTell me something, and I will repeat it back to you."
prompt += "\nEnter 'quit' to end the program: "

message = ""
while message != "quit":
    message = input(prompt)
    if message != "quit":
        print(message)

# Using a Flag
prompt = "\nTell me something, and I will repeat it back to you."
prompt += "\nEnter 'quit' to end the program: "

active = True # This is the flag
while active:
    message = input(prompt)
    if message == 'quit':
        active = False # This is the flag
    else:
        print(message)

# Using break to Exit a Loop
prompt = "\nPlease enter the name of a city you have visited: "
prompt += "\n(Enter 'quit' when you are finished.) "

while True:
    city = input(prompt)

    if city == 'quit':
        break
    else:
        print(f"I'd love to go to {city.title()}!")

# Using continue in a Loop
current_number = 0
while current_number < 10:
    current_number += 1
    if current_number % 2 == 0:
        continue # This skips the rest of the loop and returns to the top of the loop

    print(current_number)
```
### Using a while Loop with Lists and Dictionaries
```python
# Moving Items from One List to Another

# Start with users that need to be verified,
# and an empty list to hold confirmed users.
unconfirmed_users = ['alice', 'brian', 'candace']
confirmed_users = []

# Verify each user until there are no more unconfirmed users.
# Move each verified user into the list of confirmed users.
while unconfirmed_users:
    current_user = unconfirmed_users.pop()

    print(f"Verifying user {current_user.title()}...")
    confirmed_users.append(current_user)

# Display all confirmed users.
print("\nThe following users have been confirmed:")
for confirmed_user in confirmed_users:
    print(f"✓ {confirmed_user.title()}")

# Removing All Instances of Specific Values from a List
pets = ['dog', 'cat', 'mouse', 'rabbit', 'cat', 'goldfish', 'cat']
print(pets)

while 'cat' in pets:
    pets.remove('cat')

print(pets)

# Filling a Dictionary with User Input

responses = {}
# Set a flag to indicate that polling is active.
polling_active = True
while polling_active:
    # Prompt for the person's name an response.
    name = input("\nWhat is your name? ")
    response = input("\nWhat is your favorite programming language? ")

    # Store the response in the dictionary.
    responses[name] = response

    # Find out if anyone else is giong to take the poll.
    repeat = input("\nWould you like to let another person respond? (yes/no) ")
    if repeat == 'no':
        polling_active = False

# Polling is complete. Show the results.
print("\n--- Poll Results ---")
for name, response in responses.items():
    print(f"{name}'s favorite programming language is {response}.")

# Rachael's Sandwich Ordering Program
sandwich_orders = {}

order_active = True
while order_active:
    name = input("Enter your name: ")
    sandwich_type = input('Choose a sandwich type: Ham, Turkey, Tuna ')
    bread_type = input('Choose a bread type: White, Wheat, Rye ')

    sandwich_orders[name] = (sandwich_type, bread_type)

    repeat = input('\nWould you like to let another person order? yes/no ')
    if repeat == 'no':
        order_active = False

print("\n--- Sandwich Orders ---")
for name, (sandwich_type, bread_type) in sandwich_orders.items():
    print(f"{name} ordered a {sandwich_type} sandwich on {bread_type}.")

```
## Functions
- [Return Values](#return-values)
- [Passing a List](#passing-a-list)
- [Passing an Arbitaray Number of Arguments](#passing-an-arbitaray-number-of-arguments)
- [Storing Your Functions in Modules](#storing-your-functions-in-modules)
```python
# Defining a Function
def greet_user():
    """Display a simple greeting"""
    print("Hello User!")


greet_user()
# Output = Hello User!

# Passing information into a Function
# Defining a Function
def greet_user(name):
    """Display a simple greeting"""
    print(f"Hello {name.title()}!")


greet_user('rachael')
# # Output = Hello Rachael!

greet_user('phil')
# Output = Hello Phil!

# Positional Arguments
def describe_pet(animal_type, pet_name):
    """Display information about a pet"""
    print(f"I have a {animal_type}.")
    print(f"My {animal_type}'s name is {pet_name.title()}")


describe_pet('fish', 'wanda')
# Output = I have a fish.
# My fish's name is Wanda

# You can make multiple function calls...
describe_pet('cat', 'olive')
# Output = I have a cat.
# My cat's name is Olive

# Order matters in positional arguments...
describe_pet('wanda', 'fish')
# Output = I have a wanda.
# My wanda's name is Fish

# Keyword Arguments
def describe_pet(animal_type, pet_name):
    """Display information about a pet"""
    print(f"I have a {animal_type}.")
    print(f"My {animal_type}'s name is {pet_name.title()}")


animal_type_input = input("Enter your pet's animal type: ")
pet_name_input = input("Enter your pet's name: ")

describe_pet(animal_type=animal_type_input, pet_name=pet_name_input)
# Output = I have a dog.
# My dog's name is Cesar

# If you're using positional arguments, order of arguments matters.
# If you're using keyword arguments, you just have to match the 
# right keyword with the right piece of data.

# Default Values
def describe_pet(pet_name, animal_type='dog'):
    """Display information about a pet"""
    print(f"I have a {animal_type}.")
    print(f"My {animal_type}'s name is {pet_name.title()}.")


describe_pet(pet_name='wanda', animal_type='fish')
# Output = I have a fish.
# My fish's name is Wanda.

describe_pet('cesar')
# Output = I have a dog.
# My dog's name is Cesar.

# Equivalent Function Calls
def describe_pet(pet_name, animal_type='dog'):
    """Display information about a pet"""
    print(f"I have a {animal_type}.")
    print(f"My {animal_type}'s name is {pet_name.title()}.")


# A dog named Willie.
describe_pet('willie')
# Output = I have a dog.
# My dog's name is Willie.

# A hamster named Harry.
describe_pet('harry', 'hamster')
describe_pet(pet_name='harry', animal_type='hamster')
describe_pet(animal_type='hamster', pet_name='harry')
# Output = I have a hamster.
# My hamster's name is Harry.

# Rachael's Custom T-shirt Example
def custom_tshirt(size, message):
    """Display t-shirt size and customization"""
    print(f"T-shirt size: {size.upper()}")
    print(f"Customization: {message.title()}")
    print("Thank you for ordering a custom t-shirt!")


tshirt_size = input("Enter t-shirt size (s/m/l/xl/xxl): ")
tshirt_message = input("Enter custom message to apply to t-shirt: ")

custom_tshirt(tshirt_size, tshirt_message)
```
### Return Values
```python
# Return a Simple Value
def get_formatted_name(first_name, last_name):
    """Return a full name, neatly formatted."""
    full_name = f"{first_name} {last_name}"
    return full_name.title()


musician = get_formatted_name('jimi', 'hendrix')
print(musician)
# Output = Jimi Hendrix

# Making an Argument Optional
def get_formatted_name(first_name, last_name, middle_name=''):
    """Return a full name, neatly formatted."""
    full_name = f"{first_name} {middle_name} {last_name}"
    return full_name.title()


musician = get_formatted_name('john', 'hooker', 'lee')
print(musician)
# Output = John Lee Hooker

musician = get_formatted_name('jimi', 'hendrix')
print(musician)
# Output = Jimi  Hendrix

# Returning a Dictionary
def build_person(first_name, last_name):
    """Return a dictionary of information about a person."""
    person = {'first': first_name, 'last': last_name}
    return person


musician = build_person('jimi', 'hendrix')
print(musician)
# Output = {'first': 'jimi', 'last': 'hendrix'}

# Returning a Dictionary with Optional Parameter
def build_person(first_name, last_name, age=None):
    """Return a dictionary of information about a person."""
    person = {'first': first_name, 'last': last_name}
    if age:
        person['age'] = age
    return person


musician = build_person('jimi', 'hendrix', '27')
print(musician)
# Output = {'first': 'jimi', 'last': 'hendrix', 'age': '27'}

# Using a Function with a while Loop
def get_formatted_name(first_name, last_name):
    """Return a full name, neatly formatted."""
    full_name = f"{first_name} {last_name}"
    return full_name.title()

# This is an infinite loop and should only be used
# for test and demonstration purposes!!!
while True:
    print("\nPlease tell me your name...")
    f_name = input("First Name: ")
    l_name = input("Last Name: ")

    formatted_name = get_formatted_name(f_name, l_name)
    print(f"\nHello, {formatted_name}!")
# Output = Hello, Rachael Pracht!

# Using a Function with a while Loop
def get_formatted_name(first_name, last_name):
    """Return a full name, neatly formatted."""
    full_name = f"{first_name} {last_name}"
    return full_name.title()

# Let's break the infinite loop in this function
while True:
    print("\nPlease tell me your name...")
    print("enter 'q' at any time to quit")

    f_name = input("First Name: ")
    if f_name == 'q':
        break
    l_name = input("Last Name: ")
    if l_name == 'q':
        break

    formatted_name = get_formatted_name(f_name, l_name)
    print(f"\nHello, {formatted_name}!")
```
### Passing a List
```python
def greet_users(names):
    """Print a simple greeting to each user in the list."""
    for name in names:
        msg = f"Hello, {name.title()}!"
        print(msg)


usernames = ['hannah', 'ty', 'margot']
greet_users(usernames)
# Output = Hello, Hannah!
# Hello, Ty!
# Hello, Margot!

# Modifying a List in a Function
def print_models(unprinted_designs, completed_models):
    """Simulate printing each design, until none are left.
    Move each design to completed models after printing."""
    while unprinted_designs:
        while unprinted_designs:
            current_design = unprinted_designs.pop()
            print(f"Printing model: {current_design}...")
            completed_models.append(current_design)


def show_completed_models(completed_models):
    """Show all the models that were printed."""
    print(f"\nThe following models have been printed")
    for completed_model in completed_models:
        print(completed_model)


unprinted_designs = ['phone case', 'robot pendant', 'dodecahedron']
completed_models = []

print_models(unprinted_designs, completed_models)
show_completed_models(completed_models)

# Preventing a Function from Modifying a List
# You can use a copy of a list to enter into the function
# instead of changing the original list.
# You would change the function like this:
# print_models(unprinted_designs[:], completed_models)
```
### Passing an Arbitaray Number of Arguments
```python
def make_pizza(*toppings):
    """Print the list of toppings that have been requested."""
    print("\nMaking a pizza with the following toppings:")
    for topping in toppings:
        print(f"- {topping}")


make_pizza('pepperoni')
make_pizza('mushrooms', 'green peppers', 'extra cheese')

# The * in the parameter tells Python to make a 
# tuple and contain all values passed into the function

# Mixing Positional and Arbitrary Arguments
def make_pizza(size, *toppings):
    """Print the list of toppings that have been requested."""
    print(f"\nMaking a {size}-inch pizza with the following toppings:")
    for topping in toppings:
        print(f"- {topping}")


make_pizza(16, 'pepperoni')
make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')

# The parameter that accepts an arbitrary number
# of arguments must be placed last
# You'll often see the generic parameter named *args,
# which collects arbitrary positional arguments like this.

# Using Arbitrary Keyword Arguments
def build_profile(first, last, **user_info):
    """Build a dictionary containing everything we know about a user."""
    user_info['first_name'] = first
    user_info['last_name'] = last
    return user_info


user_profile = build_profile('albert', 'einstein',
                             location='princeton',
                             field='pysics')

print(user_profile)

# You'll often see the parameter name **kwargs used to
# collect nonspecific keyword arguments.
```
### Storing Your Functions in Modules
```python
# Importing an Entire Module

# In the main file... (practice.py)
import pizza

pizza.make_pizza(16, 'pepperoni')
pizza.make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')

# In the 'import pizza' file... (pizza.py)
def make_pizza(size, *toppings):
    """Print the list of toppings that have been requested."""
    print(f"\nMaking a {size}-inch pizza with the following toppings:")
    for topping in toppings:
        print(f"- {topping}")

# Importing Specific Functions
# Syntax: from module_name import function_name1, function_name2 (etc.)
from pizza import make_pizza

make_pizza(16, 'pepperoni')
make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')

# Using 'as' to Give a Function an Alias

from pizza import make_pizza as mp

mp(16, 'pepperoni')
mp(12, 'mushrooms', 'green peppers', 'extra cheese')

# Using 'as' to Give a Module an Alias

import pizza as p
p.make_pizza(16, 'pepperoni')
p.make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')

# Importing All Functions in a Module
from pizza import *
make_pizza(16, 'pepperoni')
make_pizza(12, 'mushrooms', 'green peppers', 'extra cheese')
```
## Classes
- [Working with Classes & Instances](#)
- [Inheritance](#)
- [Importing Classes](#)
- [The Python Standard Library](#)
```python
```
### Working with Classes & Instances
```python
```
### Inheritance
```python
```
### Importing Classes
```python
```
### The Python Standard Library
```python
```
