# Boolean Variables

A Boolean (`bool`) has only two possible values: `True` or `False`.

```python
is_ready = True
is_finished = False
```

Python Boolean literals always begin with a capital letter.

## Comparisons

```python
print(10 > 5)
print(10 == 5)
print(7 != 8)
```

## Logical operators

```python
age = 20
has_ticket = True

print(age >= 18 and has_ticket)
print(age < 18 or has_ticket)
print(not has_ticket)
```

The `and`, `or`, and `not` operators combine or negate Boolean expressions.

## Truth and falsiness

Some values are considered false in Boolean contexts:

```python
print(bool(False))
print(bool(None))
print(bool(0))
print(bool(""))
print(bool([]))
```

Non-empty strings and lists are generally true:

```python
print(bool("Python"))
print(bool([1, 2, 3]))
```

## Using Booleans with conditions

```python
is_raining = True

if is_raining:
    print("Take an umbrella.")
else:
    print("Leave the umbrella at home.")
```

## Boolean conversion

```python
print(bool("False"))
print(bool(""))
```

The string `"False"` is not `False`; it is a non-empty string and therefore truthy.

## Identity and equality

Use `==` to compare values and `is` to compare object identity:

```python
print(10 == 10.0)
print(10 is 10)
```

Avoid `is` for ordinary values such as integers and strings; use `is` mainly for `None` or object identity checks:

```python
value = None
print(value is None)
```

## Practical questions

1. Store `is_member = True` and print its type.
2. Ask whether 25 is greater than 30.
3. Create `age = 15` and `has_permission = True`; print whether either condition allows attendance.
4. Write a Boolean expression that is `True` only when a number is between 10 and 20 inclusive.
5. Print which of `0`, `""`, `[]`, `"0"`, and `[0]` are true or false.
