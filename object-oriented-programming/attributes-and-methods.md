# Attributes and Methods

## Instance attributes

Instance attributes belong to a specific object:

```python
class Car:
    def __init__(self, brand):
        self.brand = brand
```

## Instance methods

Instance methods operate on an object and use `self`:

```python
class Car:
    def __init__(self, brand):
        self.brand = brand

    def drive(self):
        print(f"The {self.brand} is driving")

car = Car("Toyota")
car.drive()
```

## Class attributes

```python
class Circle:
    pi = 3.14159

print(Circle.pi)
```

## Class methods

```python
class Employee:
    employee_count = 0

    def __init__(self, name):
        self.name = name
        Employee.employee_count += 1

    @classmethod
    def count(cls):
        return cls.employee_count
```

## Static methods

```python
class Temperature:
    @staticmethod
    def celsius_to_fahrenheit(celsius):
        return celsius * 9 / 5 + 32

print(Temperature.celsius_to_fahrenheit(25))
