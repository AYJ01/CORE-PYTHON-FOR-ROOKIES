# Dictionary Methods

## Common methods

```python
student = {"name": "Asha", "score": 92}

print(student.keys())
print(student.values())
print(student.items())
print(student.get("grade", "N/A"))
```

## Set default

```python
student.setdefault("grade", "Pending")
print(student)
```

## Merge dictionaries

```python
academic = {"name": "Asha", "score": 92}
personal = {"city": "Mumbai", "age": 20}

academic.update(personal)
combined = {**academic, "passed": True}
```

## Copy

```python
copy = student.copy()
```
