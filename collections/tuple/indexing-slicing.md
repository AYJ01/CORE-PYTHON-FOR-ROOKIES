# Tuple Indexing and Slicing

## Indexing

```python
names = ("Asha", "Ben", "Chen")

print(names[0])
print(names[-1])
```

## Immutability

Tuple elements cannot be reassigned:

```python
values = (10, 20, 30)
# values[1] = 25  # raises TypeError
```

## Slicing

```python
numbers = (0, 1, 2, 3, 4, 5)

print(numbers[1:4])
print(numbers[:3])
print(numbers[3:])
print(numbers[::2])
print(numbers[::-1])
```

Slicing a tuple creates a tuple.
