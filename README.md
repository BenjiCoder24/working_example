# Python Tutorial for Beginners

## Introduction

This tutorial will guide you through the basics of Python, focusing on functions, variables, and for loops.

## Variables

Variables are used to store information that can be referenced and manipulated in a program.


```python
# Creating a variable

greeting = 'Hello, world!'

print(greeting)
```

## Functions

Functions are reusable pieces of code that perform a specific task.


```python
# Defining a function

def greet(name):

    print(f'Hello, {name}!')



greet('Alice')
```

## For Loops

For loops are used for iterating over a sequence (such as a list, tuple, dictionary, or string).

```python
# Using a for loop

colors = ['red', 'green', 'blue']

for color in colors:

    print(color)
```

## Fully Working Example

Now, let's combine what we've learned into a fully working example.


```python
# A simple program that greets each person in a list by their favorite color

def greet_by_favorite_color(name, color):

    print(f'Hello, {name}! Your favorite color is {color}.')



names_and_colors = [('Alice', 'blue'), ('Bob', 'green'), ('Charlie', 'red')]

for name, color in names_and_colors:

    greet_by_favorite_color(name, color)
```

