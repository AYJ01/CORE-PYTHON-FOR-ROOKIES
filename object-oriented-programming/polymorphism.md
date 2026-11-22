# Polymorphism

Polymorphism allows objects of different classes to respond through a common interface.

```python
class Dog:
    def speak(self):
        return "Woof"

class Cat:
    def speak(self):
        return "Meow"

animals = [Dog(), Cat()]

for animal in animals:
    print(animal.speak())
```

## Duck typing

Python uses behavior rather than requiring a strict inheritance relationship:

```python
class TextWriter:
    def write(self, text):
        print(text)

class FileWriter:
    def write(self, text):
        with open("output.txt", "a") as file:
            file.write(text)

def save(writer, text):
    writer.write(text)
```

## Abstract base classes

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Square(Shape):
    def __init__(self, side):
        self.side = side

    def area(self):
        return self.side * self.side
