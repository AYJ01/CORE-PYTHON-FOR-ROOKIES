# Try and Except

Use `try` around code that might raise an exception and `except` to handle it.

```python
try:
    value = int("not a number")
except ValueError:
    print("Invalid integer")
```

## Multiple exception types

```python
try:
    number = int(input("Number: "))
    print(10 / number)
except (ValueError, ZeroDivisionError):
    print("Enter a valid non-zero integer.")
```

## Separate handlers

```python
try:
    number = int(input("Number: "))
    print(10 / number)
except ValueError:
    print("Not an integer")
except ZeroDivisionError:
    print("Cannot divide by zero")
```

## Catching the exception object

```python
try:
    result = 10 / 0
except ZeroDivisionError as error:
    print(type(error).__name__, error)
```
