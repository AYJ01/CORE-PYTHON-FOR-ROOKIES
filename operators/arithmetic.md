# Arithmetic Operators

Arithmetic operators perform mathematical calculations.

| Operator | Meaning | Example | Result |
|---|---|---|---|
| `+` | Addition | `10 + 3` | `13` |
| `-` | Subtraction | `10 - 3` | `7` |
| `*` | Multiplication | `10 * 3` | `30` |
| `/` | Division | `10 / 3` | `3.333...` |
| `//` | Floor division | `10 // 3` | `3` |
| `%` | Remainder | `10 % 3` | `1` |
| `**` | Exponentiation | `10 ** 3` | `1000` |

## Division and floor division

```python
print(10 / 4)
print(10 // 4)
print(-10 // 4)
```

Division using `/` produces a `float`. Floor division produces the quotient rounded toward negative infinity.

## Remainder

The remainder operator is useful for even/odd checks and cyclic values:

```python
number = 17
print(number % 2)

for number in range(1, 6):
    if number % 2 == 0:
        print(number, "is even")
```

## Exponents

```python
print(2 ** 8)
print(9 ** 0.5)
```

## String repetition and concatenation

```python
print("ha" * 3)
print("Good " + "morning")
```

The `+` and `*` operators also work with some sequences.

## Practical questions

1. Store `a = 24` and `b = 7`; print all seven arithmetic results.
2. Calculate the area of a rectangle using variables.
3. Use `%` to determine whether a number is even or odd.
4. Convert 3665 seconds into hours, minutes, and seconds.
5. Calculate `5` raised to the power `4`.
