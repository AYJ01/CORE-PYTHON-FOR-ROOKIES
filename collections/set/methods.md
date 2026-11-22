# Set Methods

## Adding values

```python
languages = {"Python"}
languages.add("Java")
languages.update(["Rust", "Go"])
```

## Removing values

```python
languages = {"Python", "Java", "Rust"}
languages.remove("Java")
languages.discard("C")
removed = languages.pop()
languages.clear()
```

- `remove()` raises `KeyError` if the value is absent.
- `discard()` does nothing if the value is absent.
- `pop()` removes an unspecified value.

## Comparison methods

```python
small = {1, 2}
large = {1, 2, 3}

print(small.issubset(large))
print(large.issuperset(small))
print(small.isdisjoint({3, 4}))
```
