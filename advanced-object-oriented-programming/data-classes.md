# Data Classes

The `dataclasses` module generates common methods for classes that primarily store data.

```python
from dataclasses import dataclass

@dataclass
class Student:
    name: str
    score: int

student = Student("Asha", 92)
print(student)
print(student == Student("Asha", 92))
```

## Default values

```python
@dataclass
class Settings:
    theme: str = "light"
    notifications: bool = True
```

## Frozen data classes

```python
@dataclass(frozen=True)
class Coordinate:
    x: float
    y: float
```

Frozen instances cannot have their fields reassigned after creation.
