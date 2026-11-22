# Access and Updates

## Accessing values

```python
student = {"name": "Asha", "score": 92}

print(student["name"])
print(student.get("grade", "Not assigned"))
```

Using `[]` with a missing key raises `KeyError`. `get()` returns `None` or a supplied default instead.

## Adding and updating values

```python
student["age"] = 20
student["score"] = 95
student.update({"grade": "A", "passed": True})
```

## Removing values

```python
age = student.pop("age")
item = student.popitem()
del student["grade"]
student.clear()
```

- `pop()` removes a specified key.
- `popitem()` removes the last inserted key-value pair.
- `del` removes a specified key.
- `clear()` removes every entry.
