# Assertions

An assertion checks whether a condition is true.

```python
value = 10
assert value > 0
```

If the condition is false, Python raises `AssertionError`:

```python
assert 2 + 2 == 5
```

Do not rely on `assert` for validating user input in production code. It can be disabled with optimized Python execution. Use exceptions and normal validation instead.
