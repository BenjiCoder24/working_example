
# Python Functions and Exception Handling Tutorial

## how to open the codeing environement

open:
<a href="https://colab.research.google.com/drive/1RYQp-m3nOEZCMEF4VeKfzwaTHSQ3Lbme?usp=sharing" target="_blank">Click here to open Google Colab</a>


## Introduction to Python Functions

Functions are the building blocks of readable, maintainable, and reusable code. They allow you to execute a block of code multiple times without repeating yourself.

```python
def greet(name):
    print(f"Hello, {name}!")
greet('Alice')
```

## Understanding Function Return Values

Functions can return values that can be used later in the code.

```python
def add(a, b):
    return a + b
result = add(3, 4)
print(result)
```

## Scope and Lifetime of Variables

Variables created inside a function are local to that function, unless declared global.

```python
def function_scope():
    local_var = 5
    print(local_var)  # prints 5

local_var = 10
function_scope()  # This will print 5
print(local_var)  # This will print 10
```

## Advanced Function Concepts

You can set default values for parameters and use keyword arguments to make your functions more flexible.

```python
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")
greet('Bob')
greet('Bob', greeting='Good morning')
```

## Lambda Functions

Lambda functions are small anonymous functions that can have any number of arguments but only one expression.

```python
square = lambda x: x ** 2
print(square(5))
```

## Decorators and Higher-Order Functions

Decorators are a way to modify the behavior of a function without permanently modifying it.

```python
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

say_hello()
```

## Introduction to Exception Handling

Exception handling in Python is done through the use of try and except blocks.

```python
try:
    # code that may cause an exception
    number = int(input("Enter a number: "))
except ValueError:
    print("That's not a valid number!")
```

## Working with the Exception Hierarchy

Python has many built-in exceptions that you can use to handle different error cases.

```python
try:
    # code that may cause an exception
    number = int(input("Enter a number: "))
except ValueError as e:
    print(f"An error occurred: {e}")
```

## Ensuring Resource Management with `with` Statements

The with statement allows you to ensure that resources are properly managed.

```python
with open('file.txt', 'w') as file:
    file.write('Hello, world!')
```

## Practical Example: Creating a Robust Function

Let's build a function that takes user input and handles errors appropriately.

```python
def get_number():
    while True:
        try:
            return int(input("Enter a number: "))
        except ValueError:
            print("That's not a valid number! Please try again.")

number = get_number()
print(f"You entered: {number}")
```

## Conclusion

In this tutorial, we've covered how to define and use functions, handle exceptions, and manage resources in Python. These concepts are essential for writing clean, efficient, and robust Python code.
