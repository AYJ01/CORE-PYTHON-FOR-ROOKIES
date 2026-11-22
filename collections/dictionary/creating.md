# Creating Dictionaries

## Literal syntax

```python
student = {
    "name": "Asha",
    "age": 20,
    "score": 92,
}
```

## Empty dictionary

```python
empty = {}
empty_too = dict()
```

## Dictionary constructor

```python
student = dict(name="Asha", age=20, score=92)
```

Keys and values can also come from sequences:

```python
keys = ["name", "age", "score"]
values = ["Asha", 20, 92]
student = dict(zip(keys, values))
```

## Nested dictionaries

```python
students = {
    "s1": {"name": "Asha", "score": 92},
    "s2": {"name": "Ben", "score": 88},
}
```
