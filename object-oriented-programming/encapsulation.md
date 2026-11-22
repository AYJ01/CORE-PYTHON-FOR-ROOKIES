# Encapsulation

Encapsulation limits direct access to an object's internal state.

## Public attribute

```python
class Wallet:
    def __init__(self, balance):
        self.balance = balance
```

## Protected convention

A single underscore indicates that an attribute is intended for internal use:

```python
class Account:
    def __init__(self, balance):
        self._balance = balance
```

## Private convention

Double underscores trigger name mangling:

```python
class Account:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def get_balance(self):
        return self.__balance
```

## Properties

```python
class Temperature:
    def __init__(self, celsius):
        self._celsius = celsius

    @property
    def fahrenheit(self):
        return self._celsius * 9 / 5 + 32

    @fahrenheit.setter
    def fahrenheit(self, value):
        self._celsius = (value - 32) * 5 / 9
