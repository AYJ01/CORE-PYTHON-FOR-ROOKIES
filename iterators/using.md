# Using Iterators

## Creating an iterator

```python
values = ["red", "green", "blue"]
iterator = iter(values)
```

## Retrieving values

```python
print(next(iterator))
print(next(iterator))
print(next(iterator))

try:
    print(next(iterator))
except StopIteration:
    print("No more values")
```

## Iterating with a loop

```python
values = iter((1, 2, 3, 4))

for value in values:
    print(value)
```

The loop handles `StopIteration` automatically.

## Iterators versus iterables

- A list is iterable but is not an iterator.
- `iter(list)` creates a list iterator.
- Calling `iter(iterator)` normally returns the same iterator.
