# Set Comprehensions

## Transforming values

```python
squares = {number ** 2 for number in range(1, 6)}
print(squares)
```

## Filtering values

```python
evens = {number for number in range(1, 11) if number % 2 == 0}
print(evens)
```

## Removing duplicates and normalizing

```python
names = ["Asha", "Ben", "Asha", "Chen"]
unique_names = {name.lower() for name in names}
print(unique_names)
```
