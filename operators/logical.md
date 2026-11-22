# Logical Operators

Logical operators combine or invert Boolean expressions.

| Operator | Meaning | Example |
|---|---|---|
| `and` | True only when both operands are true | `age >= 18 and has_ticket` |
| `or` | True when at least one operand is true | `is_member or is_staff` |
| `not` | Reverses a Boolean value | `not is_blocked` |

## and

```python
age = 20
has_ticket = True
print(age >= 18 and has_ticket)
```

Both expressions must be true.

## or

```python
is_member = False
is_staff = True
print(is_member or is_staff)
```

Only one expression needs to be true.

## not

```python
is_blocked = False
print(not is_blocked)
```

## Truth values

Logical operators return operands in some cases, not only `True` or `False`:

```python
print(0 and "Python")
print("Python" and "Code")
print("" or "Default")
print("Python" or "Default")
```

Python evaluates `and` and `or` with short-circuit behavior:

```python
active = False
print(active and 10 / 0)
```

The division is not evaluated because `active` is already false.

## Combining conditions

Use parentheses to clarify complex expressions:

```python
age = 21
has_ticket = True
is_banned = False

can_enter = age >= 18 and has_ticket and not is_banned
print(can_enter)
```

## Practical questions

1. Create `age = 15` and `has_permission = True`; print whether both allow attendance.
2. Create `is_member = False` and `is_guest = True`; print whether either grants access.
3. Negate a Boolean variable with `not`.
4. Build a condition for a number below `10` or above `20`.
5. Prevent an age from being below `0` or above `120`.
