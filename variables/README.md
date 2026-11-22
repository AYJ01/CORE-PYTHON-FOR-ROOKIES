# Python Variables

Variables give names to values stored in a Python program. Python creates a variable the first time you assign a value to its name.

## Creating a variable

```python
age = 18
name = "Ayaan"
height = 172.5
is_student = True
```

Here:

- `age` stores an integer.
- `name` stores a string.
- `height` stores a floating-point number.
- `is_student` stores a Boolean value.

## Reading a variable

```python
age = 18
print(age)
print("Age:", age)
```

When `print()` receives a variable, it displays the value currently assigned to it.

## Changing a variable

A variable can receive a new value with another assignment:

```python
score = 10
print(score)

score = 25
print(score)
```

The previous value is replaced; Python does not retain it as part of the variable.

## Dynamic typing

Python determines a variable's type from the assigned value. It can also change the variable to a different type later:

```python
value = 10
print(type(value))

value = "ten"
print(type(value))
```

This is called dynamic typing. Dynamic typing is flexible, but clear variable names and intentional assignments help prevent mistakes.

## Variable names

Choose names that describe their purpose:

```python
user_name = "Maya"
total_price = 499.50
is_logged_in = False
```

Use:

- lowercase letters
- underscores between words
- nouns or descriptive phrases
- names that make sense in the program

Avoid:

- `1st_name`
- `user-name`
- reserved Python keywords such as `for`, `class`, or `return`

Python convention uses `snake_case` for ordinary variable names.

## Multiple assignment

```python
x, y = 10, 20
print(x, y)

red = green = blue = 255
print(red, green, blue)
```

Multiple assignment can be convenient, but avoid it when it makes code harder to understand.

## Constant-style names

Python has no built-in constant type. By convention, values intended not to change use uppercase names:

```python
PI = 3.14159
MAX_USERS = 100
```

This communicates intent, but the name can still technically be reassigned.

## Swapping values

Python can swap two variables without a temporary variable:

```python
a = 1
b = 2

a, b = b, a
print(a, b)
```

## Deleting a variable

Use `del` to remove a variable name:

```python
points = 12
del points

# print(points) would cause a NameError
```

Deleting variables is rarely necessary in small programs.

## Practical exercises

1. Create variables for a person's name, age, height, and student status. Print all four values.
2. Start with `temperature = 20`, print it, change it to `24.5`, and print it again.
3. Use `type()` to display the types of `42`, `3.14`, `"Python"`, and `False`.
4. Swap two variables using tuple assignment.
5. Create one valid and one invalid variable name. Test and explain the result.

## In this directory

- [Integer](integer.md)
- [Float](float.md)
- [String](string.md)
- [Boolean](boolean.md)
- [Type conversion](type-conversion.md)
- [Practical questions](practical-questions.md)
