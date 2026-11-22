# Inheritance

Inheritance lets a class reuse and extend another class.

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print("The animal makes a sound")

class Dog(Animal):
    def speak(self):
        print("Woof")

dog = Dog("Max")
print(dog.name)
dog.speak()
```

## Using `super()`

```python
class Person:
    def __init__(self, name):
        self.name = name

class Employee(Person):
    def __init__(self, name, employee_id):
        super().__init__(name)
        self.employee_id = employee_id
```

## Multiple inheritance

```python
class Flyer:
    def fly(self):
        print("Flying")

class Swimmer:
    def swim(self):
        print("Swimming")

class Duck(Flyer, Swimmer):
    pass
```

Prefer simple inheritance hierarchies and explicit composition when relationships are not clearly hierarchical.
