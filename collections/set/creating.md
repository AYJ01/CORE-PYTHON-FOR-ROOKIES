# Creating Sets

## Literal syntax

```python
colors = {"red", "green", "blue"}
numbers = {1, 2, 3}
```

## Empty set

Use `set()`, not `{}`, to create an empty set:

```python
empty = set()
```

## Set constructor

```python
letters = set("Python")
numbers = set([1, 2, 2, 3])
```

Duplicates are removed automatically:

```python
print(set([1, 1, 2, 2, 3]))
```
