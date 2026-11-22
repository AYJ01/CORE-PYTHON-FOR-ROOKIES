# Float Variables

A float (`float`) represents a number with a fractional or decimal part.

```python
height = 172.5
weight = 68.0
temperature = -2.75
scientific = 1.5e3
```

`1.5e3` means `1.5 × 10³`, or `1500.0`.

## Checking floats

```python
price = 49.99
print(price)
print(type(price))
```

## Float operations

```python
price = 19.50
quantity = 3

subtotal = price * quantity
print(subtotal)
```

## Floating-point precision

Decimal floats are approximations in binary. Small rounding differences can occur:

```python
print(0.1 + 0.2)
print(0.1 + 0.2 == 0.3)
```

Do not compare two sensitive decimal calculations directly when exact equality matters. For many decimal applications, use the `Decimal` class:

```python
from decimal import Decimal

print(Decimal("0.1") + Decimal("0.2") == Decimal("0.3"))
```

## Rounding

```python
value = 17.567
print(round(value, 2))
```

## Converting to float

```python
print(float("12.5"))
print(float(12))
```

Invalid strings, such as `"hello"`, cannot be converted with `float()` and raise a `ValueError`.

## Practical questions

1. Store a product price and calculate its 18% tax.
2. Convert `"75.5"` into a float and print it with 1 decimal place.
3. Calculate the average of `9.5`, `8.0`, and `10.0`.
4. Round `23.8765` to two decimal places.
5. Calculate the circumference of a circle using `radius = 7.25` and `PI = 3.14159`.
