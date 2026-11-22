# Function Parameters

## Positional arguments

```python
def describe(name, age):
    print(name, "is", age, "years old")

describe("Asha", 20)
```

## Keyword arguments

```python
describe(name="Ben", age=22)
```

## Default parameters

```python
def greet(name, greeting="Hello"):
    print(greeting, name)

greet("Asha")
greet("Ben", "Welcome")
```

## Arbitrary positional arguments

```python
def total(*numbers):
    result = 0
    for number in numbers:
        result += number
    return result

print(total(10, 20, 30))
```

## Arbitrary keyword arguments

```python
def display_profile(**details):
    for key, value in details.items():
        print(key, value)

display_profile(name="Asha", age=20)
```

## Keyword-only parameters

```python
def subtract(*, minuend, subtrahend):
    return minuend - subtrahend

print(subtract(minuend=10, subtrahend=3))
