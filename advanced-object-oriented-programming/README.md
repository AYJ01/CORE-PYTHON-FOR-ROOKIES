# Advanced Object-Oriented Programming

Advanced OOP includes composition, abstraction, data classes, metaprogramming, and object lifecycle control.

## Navigation

- [Repository README](../README.md)
- [Advanced OOP](README.md)
- [Composition](composition.md)
- [Abstract base classes](abstract-base-classes.md)
- [Data classes](data-classes.md)
- [Context managers](context-managers.md)
- [Descriptors](descriptors.md)
- [Metaclasses](metaclasses.md)
- [Practical questions](practical-questions.md)

## Example

```python
from dataclasses import dataclass

@dataclass
class Point:
    x: float
    y: float

point = Point(3, 4)
print(point)
```
