# Higher-Order Functions

A higher-order function accepts a function as an argument, returns a function, or both.

## Accepting a function

```python
def apply(operation, value):
    return operation(value)

print(apply(lambda number: number * 2, 10))
```

## Returning a function

```python
def make_validator(minimum):
    def validate(value):
        return value >= minimum

    return validate

is_adult = make_validator(18)
print(is_adult(20))
print(is_adult(15))
```

## Built-in higher-order functions

```python
numbers = [1, 2, 3, 4, 5]

squares = list(map(lambda number: number ** 2, numbers))
evens = list(filter(lambda number: number % 2 == 0, numbers))
print(squares)
print(evens)
```

Built-in functions such as `map()`, `filter()`, and `sorted()` accept callable arguments.
