# Python Beginner's Cheat Sheet

## Python Reference Code
1. [Basics](#basics)
2. [Data Types](#data-types)
3. [Variables](#variables)
4. [Operators](#operators)
5. [Mathematical Calculations](#mathematical-calculations)
6. [Control Flow](#control-flow)
7. [Functions](#functions)
8. [Collections](#collections)
9. [Modules](#modules)
## Small Projects
1. [Life in Weeks](#life-in-weeks)
2. [Odd or Even](#odd-or-even)
3. [BMI Calculator](#bmi-calculator)
4. [Leap Year](#leap-year)
5. [Pizza Order](#pizza-order)
6. [Love Calculator](#love-calculator)
7. [Heads or Tails](#heads-or-tails)
8. [Banker Roulette](#banker-roulette)
9. [Treasure Map](#treasure-map)
10. [High Score]()
11. [Adding Even Numbers]()
12. [Fizzbuzz]()
## 100 Days of Python Projects
1. [Band Name Generator](#band-name-generator)
2. [Tip Calculator](#tip-calculator)
3. [Treasure Island](#treasure-island)
4. [Rock Paper Scissors](#rock-paper-scissors)
5. [Password Generator]()

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

#### Nested Lists
```python
# dirty_dozen = ["Strawberries", "Spinach", "Kale", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears", "Tomatoes", "Celery", "Potatoes"]

fruits = ["Strawberries", "Nectarines", "Apples", "Grapes", "Peaches", "Cherries", "Pears"] 
vegetables = ["Spinach", "Kale", "Tomatoes", "Celery", "Potatoes"]

dirty_dozen = [fruits, vegetables]

print(dirty_dozen)
# [['Strawberries', 'Nectarines', 'Apples', 'Grapes', 'Peaches', 'Cherries', 'Pears'], ['Spinach', 'Kale', 'Tomatoes', 'Celery', 'Potatoes']]
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

#### Removing Values
```python
fruits = {'apple', 'banana', 'grape'}
fruits.remove('apple')
print(fruits)
# Prints: {'banana', 'grape'}

```

## Modules
```python
# random
import random
number = random.randint(1,100)
print(number)
```

# Small Projects
## Life in Weeks
```python
age = input()

total_weeks_90 = 90 * 52
your_weeks = int(age) * 52
weeks_left = total_weeks_90 - your_weeks

print(f"You have {weeks_left} weeks left.")
```

## Odd or Even
```python
number = int(input())

if number % 2 == 0:
  print("This is an even number.")
else:
  print("This is an odd number.")
```

## BMI Calculator
```python
height = float(input())
weight = int(input())

bmi = weight / (height * height)

if bmi < 18.5:
  print(f"Your BMI is {bmi}, you are underweight.")
elif 18.5 <= bmi < 25:
  print(f"Your BMI is {bmi}, you have a normal weight.")
elif 25 <= bmi < 30:
  print(f"Your BMI is {bmi}, you are slightly overweight.")
elif 30 <= bmi < 35:
  print(f"Your BMI is {bmi}, you are obese.")
elif bmi <= 35:
  print(f"Your BMI is {bmi}, you are clinically obese.")
```

## Leap Year
```python
year = int(input())

if (year % 400 == 0):
  print("Leap year")
elif (year % 100 == 0):
  print("Not leap year")
elif (year % 4 == 0):
  print("Leap year")
else:
  print("Not leap year")
```

## Pizza Order
```python
print("Thank you for choosing Python Pizza Deliveries!")
size = input() # What size pizza do you want? S, M, or L
add_pepperoni = input() # Do you want pepperoni? Y or N
extra_cheese = input() # Do you want extra cheese? Y or N

bill = 0
if size == "S":
  bill += 15
elif size == "M":
  bill += 20
elif size == "L":
  bill += 25

if add_pepperoni == "Y" and size == "S":
  bill += 2
elif add_pepperoni == "Y":
  bill += 3

if extra_cheese == "Y":
  bill += 1

print(f"Your final bill is: ${bill}.")
```
## Love Calculator
```python
print("The Love Calculator is calculating your score...")
name1 = input() # What is your name?
name2 = input() # What is their name?

combined_names = name1 + name2
lower_names = combined_names.lower()
t = lower_names.count("t")
r = lower_names.count("r")
u = lower_names.count("u")
e = lower_names.count("e")
first_digit = t + r + u + e

l = lower_names.count("l")
o = lower_names.count("o")
v = lower_names.count("v")
e = lower_names.count("e")
second_digit = l + o + v + e

score = int(str(first_digit) + str(second_digit))

if score < 10 or score > 90:
  print(f"Your score is {score}, you go together like coke and mentos.")
elif 40 < score < 50:
  print(f"Your score is {score}, you are alright together.")
else:
  print(f"Your score is {score}.")

```

## Heads or Tails
```python
import random
random_side = random.randint(0,1)

if random_side == 1:
    print("Heads")
else:
    print("Tails")
```

## Banker Roulette
```python
# import random module
import random

# create a variable that selects a random index for the length of your list
random_index = random.randint(0, len(names) -1)

# Use the random_index to pick an item from the list
pick_name = names[random_index]

print(f"{pick_name} is going to buy the meal today!")
```

## Treasure Map
```python
line1 = ["⬜️","️⬜️","️⬜️"]
line2 = ["⬜️","⬜️","️⬜️"]
line3 = ["⬜️️","⬜️️","⬜️️"]
map = [line1, line2, line3]
print("Hiding your treasure! X marks the spot.")
position = input() # Where do you want to put the treasure?

letter = position[0].lower()
abc = ["a", "b", "c"]
letter_index = abc.index(letter)
number_index = int(position[1]) -1
map[number_index][letter_index] = "X"


print(f"{line1}\n{line2}\n{line3}")
```
## Average Height
```python
# Input a Python list of student heights
student_heights = input().split()
for n in range(0, len(student_heights)):
  student_heights[n] = int(student_heights[n])

# Find the count, sum, and average of the list
count = 0
sum = 0
for student in student_heights:
  count += 1
  sum += student

print(f"total height = {sum}")
print(f"number of students = {count}")
print(f"average height = {round(sum / count)}")
```

## High Score
```python
# Input a list of student scores
student_scores = input().split()
for n in range(0, len(student_scores)):
  student_scores[n] = int(student_scores[n])

# Loop through to find highest score
max_score = 0
for score in student_scores:
  if score > max_score:
    max_score = score

print(f"The highest score in the class is: {max_score}")
```

## Adding Even Numbers
```python
target = int(input()) # Enter a number between 0 and 1000

sum = 0
for number in range(2, target + 1):
  if number % 2 == 0:
      sum += number
print(sum)
```


## Fizzbuzz
```python
target = 100
for number in range(1, target + 1):
    if number % 3 == 0 and number % 5 == 0:
        print("FizzBuzz")
    elif number % 3 == 0:
        print("Fizz")
    elif number % 5 == 0:
        print("Buzz")
    else:
        print(number)
```

# 100 Days of Python Projects
## Band Name Generator
```python
welcome = "Welcome to the Band Name Generator."
print(welcome)

city = input("What's the name of the city you grew up in?\n")
pet = input("What's your pet's name?\n")
band_name = city + " " + pet

print(f"Your band name could be {band_name}")
```

## Tip Calculator
```python
print("Welcome to the tip calculator.")
bill = input("What was the total bill? \n$")
tip = input("What percentage tip would you like to leave?\n")
people = input("How many people to split the bill?\n")
bill_float = float(bill)
tip_float = float(tip)
people_float = float(people)

tip_percent = tip_float / 100
tip_amount = bill_float * tip_percent


total_bill = bill_float + tip_amount
bill_per_person = total_bill / people_float

final_amount = round(bill_per_person, 2)
final_amount = "{:.2f}".format(bill_per_person)

print(f"Each person should pay: ${final_amount}")
```

## Treasure Island
```python
print('''
*******************************************************************************
          |                   |                  |                     |
 _________|________________.=""_;=.______________|_____________________|_______
|                   |  ,-"_,=""     `"=.|                  |
|___________________|__"=._o`"-._        `"=.______________|___________________
          |                `"=._o`"=._      _`"=._                     |
 _________|_____________________:=._o "=._."_.-="'"=.__________________|_______
|                   |    __.--" , ; `"=._o." ,-"""-._ ".   |
|___________________|_._"  ,. .` ` `` ,  `"-._"-._   ". '__|___________________
          |           |o`"=._` , "` `; .". ,  "-._"-._; ;              |
 _________|___________| ;`-.o`"=._; ." ` '`."\` . "-._ /_______________|_______
|                   | |o;    `"-.o`"=._``  '` " ,__.--o;   |
|___________________|_| ;     (#) `-.o `"=.`_.--"_o.-; ;___|___________________
____/______/______/___|o;._    "      `".o|o_.--"    ;o;____/______/______/____
/______/______/______/_"=._o--._        ; | ;        ; ;/______/______/______/_
____/______/______/______/__"=._o--._   ;o|o;     _._;o;____/______/______/____
/______/______/______/______/____"=._o._; | ;_.--"o.--"_/______/______/______/_
____/______/______/______/______/_____"=.o|o_.--""___/______/______/______/____
/______/______/______/______/______/______/______/______/______/______/_____ /
*******************************************************************************
''')
print("Welcome to Treasure Island.")
print("Your mission is to find the treasure.") 

choice_1 = input("You've been walking for hours. You're tired and hungry, but you've come to a fork in the road. Which way do you go? left or right\n").lower()
if choice_1 == "left":
    choice_2 = input("You've made it down the fork and you've come to a lake. There is an island in the middle of the lake. You can search for a boat to get to it, or you can try to swim there. Do you 'search' or 'swim'?\n").lower()
    if choice_2 == "search":
        choice_3 = input("You arrive at the island unharmed. There is a house with 3 doors. Each door is a different color. There is one red, one yellow, and one blue. Which door do you choose?\n").lower()
        if choice_3 == "red": 
            print("You open the red door and are immediately sucked inside the room. The door slams shut behind you, locking. The room is full of fire. Your game is over.")
        elif choice_3 == "yellow":
            print("You open the yellow door. A bright light greets you. As your eyes adjust, you realize you are outside in a sunny grove. In front of you is an ornate chest. You have found the treasure. You win!")
        elif choice_3 == "blue":
            print("You open the blue door, and a room appears in front of you. You begin to walk in, but the floor was a mirage. You fall forever. Your game is over.")
        else:
            print("You attempt to open a door that doesn't exist. The doorknob explodes in your hand. Your game is over.")
    else:
        print("You dive in confidently, but you're attack by a giant lake trout. Your game is over.")
else:
    print("You start walking, but suddenly your feet fall out from under you. You've fallen into a hole. Your game is over.") 
```

## Rock Paper Scissors
```python
import random

rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇

# Rock wins against scissors.
# Scissors win against paper.
# Paper wins against rock.

player_1 = int(input("What do you choose? Type 0 for Rock, 1 for Paper or 2 for Scissors\n"))
player_2 = random.randint(0,2)

# Display what player 1 chose
if player_1 == 0:
    print("You chose rock.")
    print(rock)
elif player_1 == 1:
    print("You chose paper.")
    print(paper)
elif player_1 == 2:
    print("You chose scissors.")
    print(scissors)
else:
    print("Invalid selection. Game over.")

# Display what player 2 chose
if player_2 == 0:
    print("The computer chose rock.")
    print(rock)
elif player_2 == 1:
    print("The computer chose paper.")
    print(paper)
else:
    print("The computer chose scissors.")
    print(scissors)

# Compare player 1 vs. player 2 to see who won
if player_1 == player_2:
    print("You tied.")
elif player_1 == 0 and player_2 == 2:
    print("You win!")
elif player_1 == 2 and player_2 == 0:
    print("You lose.")
elif player_1 == 2 and player_2 == 1:
    print("You win!")
elif player_1 == 1 and player_2 == 2: 
    print("You lose.")
elif player_1 == 1 and player_2 == 0: 
    print("You win!")
elif player_1 == 0 and player_2 == 1: 
    print("You lose.")
```

## Password Generator
```python

```

