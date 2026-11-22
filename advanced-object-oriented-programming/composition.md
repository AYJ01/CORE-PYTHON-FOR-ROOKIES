# Composition

Composition builds classes from other objects instead of depending on inheritance.

```python
class Engine:
    def start(self):
        print("Engine started")

class Car:
    def __init__(self):
        self.engine = Engine()

    def start(self):
        self.engine.start()

car = Car()
car.start()
```

## Aggregation

```python
class Team:
    def __init__(self, members):
        self.members = members

members = ["Asha", "Ben", "Chen"]
team = Team(members)
```

Composition is often more flexible than inheritance because objects can be replaced or configured independently.
