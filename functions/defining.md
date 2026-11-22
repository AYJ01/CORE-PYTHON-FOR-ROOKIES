# Defining Functions

## Basic function

```python
def greet():
    print("Hello!")

greet()
```

The `def` keyword defines a function. The function name followed by parentheses calls it.

## Function with a parameter

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Asha")
greet("Ben")
```

## Function with docstring

```python
def square(number):
    """Return the square of a number."""
    return number * number

print(square(5))
```

Docstrings describe what a function does and can be accessed through `help()` or `__doc__`.

## Multiple statements

```python
def print_total(a, b):
    total = a + b
    print("The total is:", total)

print_total(10, 20)
