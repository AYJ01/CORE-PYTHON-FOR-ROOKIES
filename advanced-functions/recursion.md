# Recursion

A recursive function calls itself to solve a smaller copy of a problem.

## Factorial

```python
def factorial(number):
    if number == 0:
        return 1
    return number * factorial(number - 1)

print(factorial(5))
```

## Base and recursive cases

Every recursive function needs:

- A base case that stops recursion.
- A recursive case that moves toward the base case.

## Sum of numbers

```python
def sum_to(number):
    if number == 0:
        return 0
    return number + sum_to(number - 1)
```

## Fibonacci

```python
def fibonacci(number):
    if number <= 1:
        return number
    return fibonacci(number - 1) + fibonacci(number - 2)
```

Recursive solutions should be used when the problem has a naturally recursive structure. Very deep recursion can raise `RecursionError`.
