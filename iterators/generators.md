# Generators

A generator is a convenient way to create an iterator using `yield`.

## Number generator

```python
def count_to(maximum):
    for number in range(1, maximum + 1):
        yield number

for number in count_to(5):
    print(number)
```

A generator function pauses at `yield` and resumes on the next call to `next()`.

## Generator expression

```python
squares = (number ** 2 for number in range(1, 6))

print(next(squares))
print(list(squares))
```

## When to use generators

- Large or unbounded sequences
- Streaming data
- Pipelines of transformed values
- Computation that should be deferred until needed
