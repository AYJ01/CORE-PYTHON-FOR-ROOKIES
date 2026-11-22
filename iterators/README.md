# Python Iterators

Iterators provide a uniform way to traverse values one item at a time.

## Navigation

- [Repository README](../README.md)
- [Iterators](README.md)
- [Using iterators](using.md)
- [The iterator protocol](protocol.md)
- [Custom iterators](custom.md)
- [Generators](generators.md)
- [Common patterns](patterns.md)
- [Practical questions](practical-questions.md)

## Example

```python
numbers = iter([10, 20, 30])

print(next(numbers))
print(next(numbers))
print(next(numbers))
```

## Key ideas

- An **iterable** can be converted into an iterator with `iter()`.
- An **iterator** returns values one at a time with `next()`.
- Iterators are stateful and generally consumed once.
- `for` loops automatically obtain and advance iterators.
