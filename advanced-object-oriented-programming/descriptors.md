# Descriptors

Descriptors customize attribute access through `__get__`, `__set__`, and `__delete__` methods.

```python
class PositiveNumber:
    def __set_name__(self, owner, name):
        self.name = name

    def __get__(self, instance, owner):
        if instance is None:
            return self
        return instance.__dict__.get(self.name)

    def __set__(self, instance, value):
        if value < 0:
            raise ValueError("Value must not be negative")
        instance.__dict__[self.name] = value

class Product:
    price = PositiveNumber()

    def __init__(self, price):
        self.price = price

product = Product(100)
print(product.price)
