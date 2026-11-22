# Python Iterators and Loops

This section combines loop structures with Python iteration.

## Navigation

- [Repository README](../README.md)
- [Iterators and Loops](README.md)
- [For loops](for-loops.md)
- [While loops](while-loops.md)
- [Loop control](loop-control.md)
- [Using iterators](using.md)
- [The iterator protocol](protocol.md)
- [Custom iterators](custom.md)
- [Generators](generators.md)
- [Common patterns](patterns.md)
- [Practical questions](practical-questions.md)

## Example

```python
for number in range(1, 6):
    print(number)

count = 1
while count <= 5:
    print(count)
    count += 1
```

## Iteration categories

- `for` loops traverse iterables.
- `while` loops repeat while a condition is true.
- `iter()` creates an iterator.
- `next()` retrieves iterator values manually.
- Custom iterators implement `__iter__()` and `__next__()`.
- Generators create iterators using `yield`.
