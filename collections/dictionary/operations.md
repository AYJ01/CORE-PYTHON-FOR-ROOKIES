# Dictionary Operations

## Membership

```python
student = {"name": "Asha", "score": 92}

print("name" in student)
print("Asha" in student.values())
```

Membership tests check keys by default.

## Iteration

```python
for key in student:
    print(key)

for key, value in student.items():
    print(key, value)

for value in student.values():
    print(value)
```

## Copying

```python
original = {"name": "Asha", "scores": [92, 95]}
shallow = original.copy()
shallow["scores"].append(98)

print(original)
```

A shallow copy duplicates the outer dictionary, but nested mutable objects remain shared.
