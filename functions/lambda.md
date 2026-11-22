# Lambda Functions

A lambda is a small anonymous function.

## Syntax

```python
square = lambda number: number * number
print(square(5))
```

## Sorting with lambda

```python
students = [("Asha", 92), ("Ben", 88), ("Chen", 95)]
students.sort(key=lambda student: student[1])
print(students)
```

## Filtering with lambda

```python
numbers = [1, 2, 3, 4, 5, 6]
evens = list(filter(lambda number: number % 2 == 0, numbers))
print(evens)
```

## Transforming with lambda

```python
numbers = [1, 2, 3, 4]
squares = list(map(lambda number: number ** 2, numbers))
print(squares)
```

Lambdas are convenient for short operations. Use a named function for complex logic or code that needs to be reused.
