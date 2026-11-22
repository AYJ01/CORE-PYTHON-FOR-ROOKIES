# List Comprehensions

## Transforming values

```python
squares = [number ** 2 for number in range(1, 6)]
print(squares)
```

## Filtering values

```python
evens = [number for number in range(1, 11) if number % 2 == 0]
print(evens)
```

## Transforming strings

```python
names = ["asha", "ben", "chen"]
upper_names = [name.upper() for name in names]
print(upper_names)
```

## Nested comprehension

```python
pairs = [(x, y) for x in range(2) for y in range(3)]
```
