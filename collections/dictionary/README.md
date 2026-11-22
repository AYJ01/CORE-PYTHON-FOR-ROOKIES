# Python Dictionaries

Dictionaries store data as ordered key-value pairs.

## Navigation

- [Repository README](../../README.md)
- [Collections](../README.md)
- [Lists](../list/README.md)
- [Tuples](../tuple/README.md)
- [Sets](../set/README.md)
- [Dictionaries](README.md)
- [Creating dictionaries](creating.md)
- [Access and updates](access-updates.md)
- [Dictionary operations](operations.md)
- [Dictionary methods](methods.md)
- [Comprehensions](comprehensions.md)
- [Practical questions](practical-questions.md)

## Example

```python
student = {
    "name": "Asha",
    "age": 20,
    "score": 92,
}

print(student["name"])
print(student.get("grade", "Not assigned"))

student["score"] = 95
```

## Characteristics

- Ordered: key insertion order is preserved.
- Mutable: values and entries can change.
- Key-based: values are accessed through keys.
- Unique keys: a duplicate key replaces the earlier value.
- Hashable keys: dictionary keys must be hashable.
