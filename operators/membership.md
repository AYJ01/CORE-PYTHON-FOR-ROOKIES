# Membership Operators

Membership operators test whether a value occurs in a collection or sequence.

| Operator | Meaning | Example |
|---|---|---|
| `in` | Value exists in the collection | `3 in numbers` |
| `not in` | Value does not exist | `4 not in numbers` |

## Strings

```python
text = "Python programming"
print("Python" in text)
print("java" not in text)
```

Membership in strings is case-sensitive.

## Lists and tuples

```python
numbers = [10, 20, 30]
print(20 in numbers)
print(40 not in numbers)

coordinates = (4, 7)
print(7 in coordinates)
```

## Dictionaries

Membership checks dictionary keys by default:

```python
student = {"name": "Asha", "age": 20}
print("name" in student)
print("Asha" in student)
print("Asha" in student.values())
```

## Practical questions

1. Check whether `"o"` occurs in `"Python"`.
2. Test whether `7` is present in a list.
3. Test whether `"admin"` is absent from a tuple.
4. Check whether a key exists in a dictionary.
5. Check whether a value exists in `dictionary.values()`.
