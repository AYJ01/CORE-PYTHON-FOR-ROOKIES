# Tuple Methods

Tuples provide only two built-in methods: `count()` and `index()`.

## Count occurrences

```python
values = (1, 2, 2, 3)
print(values.count(2))
```

## Find an index

```python
names = ("Asha", "Ben", "Chen")
print(names.index("Ben"))
```

Both methods perform read-only operations. Tuples do not provide `append()`, `insert()`, `remove()`, `sort()`, or `clear()`.
