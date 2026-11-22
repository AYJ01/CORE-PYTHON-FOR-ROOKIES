# Creating Tuples

## Tuple syntax

```python
point = (10, 20)
names = ("Asha", "Ben", "Chen")
mixed = (10, "Python", True)
```

## One-item tuple

A comma is required for a single-item tuple:

```python
one_item = (42,)
not_a_tuple = (42)
```

Use `type()` to verify the result.

## Empty tuple

```python
empty = ()
```

## Tuple constructor

```python
numbers = tuple([1, 2, 3])
characters = tuple("Python")
```

## Packing and unpacking

```python
student = "Asha", 92
name, score = student
```
