# Variable Type Conversion

Type conversion changes a value from one Python type to another.

## Built-in conversion functions

```python
print(int("25"))
print(float("25"))
print(str(25))
print(bool("yes"))
```

## Converting input

The `input()` function always returns a string:

```python
age_text = input("Enter your age: ")
age = int(age_text)
print(age + 1)
```

An invalid value can stop the program:

```python
age = int("twenty")
```

Handle possible conversion errors before depending on the value:

```python
text = input("Enter a whole number: ")

try:
    number = int(text)
    print(number * 2)
except ValueError:
    print("Please enter a valid whole number.")
```

## Common conversions

| Function | Example | Result |
|---|---|---|
| `int()` | `int("12")` | `12` |
| `float()` | `float("12.5")` | `12.5` |
| `str()` | `str(12)` | `"12"` |
| `bool()` | `bool(1)` | `True` |
| `list()` | `list("abc")` | `['a', 'b', 'c']` |
| `tuple()` | `tuple([1, 2])` | `(1, 2)` |
| `set()` | `set([1, 1, 2])` | `{1, 2}` |

## Checking types

Use `type()` for an exact type:

```python
value = 12
print(type(value) is int)
```

Use `isinstance()` when subclasses may be allowed:

```python
print(isinstance(value, int))
```

## Implicit conversion

Python automatically converts some values during operations:

```python
print(10 + 2.5)
print(True + 4)
```

The Boolean `True` acts as `1` in arithmetic. For readable code, avoid relying on this behavior.

## Formatting instead of conversion

An f-string can insert numbers without converting them explicitly:

```python
quantity = 3
print(f"Quantity: {quantity}")
```

## Practical questions

1. Read two numbers as strings, convert them to integers, and print their sum.
2. Convert `"3.75"` to a float and multiply it by `4`.
3. Convert `45` to a string and print a sentence containing it.
4. Safely convert user input with `try` and `except`.
5. Compare `bool(0)` and `bool(-1)`.
