# Return Values

A function can return a value with `return`.

```python
def add(a, b):
    return a + b

result = add(10, 20)
print(result)
```

## Returning multiple values

Python can return multiple values as a tuple:

```python
def calculate(a, b):
    return a + b, a - b

addition, subtraction = calculate(10, 3)
print(addition, subtraction)
```

## Early return

```python
def divide(a, b):
    if b == 0:
        return None
    return a / b
```

## Implicit `None`

```python
def greet(name):
    print("Hello", name)

value = greet("Asha")
print(value)
```

A function that has no `return` statement returns `None`.
