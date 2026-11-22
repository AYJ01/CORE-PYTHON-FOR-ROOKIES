# Exception Handling

Exceptions are errors detected while a Python program is running. Handling them keeps programs from crashing unexpectedly and makes failures easier to diagnose.

## Navigation

- [Repository README](../README.md)
- [Exception Handling](README.md)
- [Try and except](try-and-except.md)
- [Else and finally](else-and-finally.md)
- [Built-in exceptions](built-in-exceptions.md)
- [Custom exceptions](custom-exceptions.md)
- [Raising exceptions](raising-exceptions.md)
- [Practical questions](practical-questions.md)

## Basic example

```python
try:
    number = int(input("Enter a number: "))
    print(10 / number)
except ValueError:
    print("Please enter a valid integer.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
```
