# Comparison Operators

Comparison operators compare values and return a Boolean result.

| Operator | Meaning | Example |
|---|---|---|
| `==` | Equal to | `10 == 10` |
| `!=` | Not equal to | `10 != 3` |
| `>` | Greater than | `10 > 3` |
| `<` | Less than | `10 < 3` |
| `>=` | Greater than or equal | `10 >= 10` |
| `<=` | Less than or equal | `10 <= 3` |

## Basic comparisons

```python
print(10 == 10)
print(10 != 3)
print(10 > 3)
print(10 <= 10)
```

## Comparing strings

Strings are compared lexicographically:

```python
print("apple" == "apple")
print("apple" < "banana")
```

Comparison is case-sensitive:

```python
print("Python" == "python")
```

## Chained comparisons

Python supports concise chained comparisons:

```python
age = 20
print(18 <= age <= 65)

number = 15
print(10 < number < 20)
```

This means `10 < number and number < 20`.

## Equality and identity

Use `==` for value equality:

```python
print(10 == 10.0)
```

Use `is` for identity, generally with `None`:

```python
value = None
print(value is None)
```

## Practical questions

1. Compare `25` and `30` using `>`, `<`, and `==`.
2. Check whether a user's age is at least `18`.
3. Check whether a number is between `10` and `20` inclusive.
4. Compare `"Python"` and `"python"`.
5. Determine whether two variables contain the same value.
