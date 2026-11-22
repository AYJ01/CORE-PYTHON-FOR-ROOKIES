# Integer Variables

An integer (`int`) is a whole number with no decimal point.

```python
age = 18
year = 2026
temperature = -4
large_number = 10_000_000
```

Underscores make large integer literals easier to read. Python ignores the underscores.

## Checking an integer

```python
number = 42
print(number)
print(type(number))
print(isinstance(number, int))
```

## Integer operations

```python
a = 12
b = 5

print(a + b)  # Addition: 17
print(a - b)  # Subtraction: 7
print(a * b)  # Multiplication: 60
print(a // b) # Integer division: 2
print(a % b)  # Remainder: 2
print(a ** b) # Exponent: 248832
```

`//` performs floor division. `/` always produces a `float` for normal division:

```python
print(10 / 4)  # 2.5
print(10 // 4) # 2
```

## Assignment operators

```python
score = 10
score += 5
score *= 2
print(score)
```

## Comparing integers

```python
print(10 > 5)
print(10 == 10)
print(7 <= 3)
```

Comparisons return Boolean values.

## Converting to integer

```python
print(int("25"))
print(int(3.9))
```

Converting a float with `int()` removes the fractional part. It does not round it.

## Practical questions

1. Store the number `2026` in a variable and print it with a label.
2. Calculate and print the sum, difference, product, and quotient of `18` and `4`.
3. Find the remainder when `29` is divided by `5`.
4. Use `//` to calculate how many complete teams of 6 can be formed from 40 people.
5. Print `True` if `100` is greater than `99`, otherwise print `False`.
