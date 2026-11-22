# Python Sets

Sets are unordered collections of unique values.

## Navigation

- [Repository README](../../README.md)
- [Collections](../README.md)
- [Lists](../list/README.md)
- [Tuples](../tuple/README.md)
- [Sets](README.md)
- [Creating sets](creating.md)
- [Set operations](operations.md)
- [Set methods](methods.md)
- [Comprehensions](comprehensions.md)
- [Practical questions](practical-questions.md)

## Example

```python
languages = {"Python", "Java", "JavaScript"}
languages.add("Rust")

print(languages)
print("Python" in languages)
```

## Characteristics

- Unordered: values have no positional indexes.
- Unique: duplicate values are removed.
- Mutable: values can be added and removed.
- Hashable elements: set elements must be hashable.
