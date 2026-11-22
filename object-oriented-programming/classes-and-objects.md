# Classes and Objects

A class defines attributes and methods. An object is an instance of a class.

```python
class Student:
    def __init__(self, name, score):
        self.name = name
        self.score = score

student1 = Student("Asha", 92)
student2 = Student("Ben", 88)

print(student1.name)
print(student2.score)
```

## The `__init__` method

`__init__()` initializes a new object:

```python
class Counter:
    def __init__(self):
        self.count = 0
```

## Instance objects

```python
first = Counter()
second = Counter()

first.count += 1
print(first.count)
print(second.count)
