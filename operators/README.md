# Python Operators

Operators perform actions on values, variables, and expressions.

```python
a = 10
b = 3

print(a + b)
print(a > b)
print(a and b)
```

## Navigation

- [Repository README](../README.md)
- [Variables](../variables/README.md)
- [Data types](../data-types/README.md)
- [Operators](README.md)
- [Practical questions](practical-questions.md)

## Quick reference

| Category | Operators | Reference |
|---|---|---|
| Arithmetic | `+ - * / // % **` | [Arithmetic operators](arithmetic.md) |
| Assignment | `= += -= *= /= //= %= **=` | [Assignment operators](assignment.md) |
| Comparison | `== != > < >= <=` | [Comparison operators](comparison.md) |
| Logical | `and or not` | [Logical operators](logical.md) |
| Identity | `is is not` | [Identity operators](identity.md) |
| Membership | `in not in` | [Membership operators](membership.md) |
| Bitwise | `& | ^ ~ << >>` | [Bitwise operators](bitwise.md) |
| Precedence | Controls evaluation order | [Operator precedence](precedence.md) |

## Operator categories

- [Arithmetic operators](arithmetic.md): calculate numerical values.
- [Assignment operators](assignment.md): assign or update values.
- [Comparison operators](comparison.md): compare values.
- [Logical operators](logical.md): combine Boolean expressions.
- [Identity operators](identity.md): compare object identity.
- [Membership operators](membership.md): test membership in sequences and collections.
- [Bitwise operators](bitwise.md): operate on integers at the binary level.
- [Operator precedence](precedence.md): control evaluation order.
- [Practical questions](practical-questions.md): combined practice exercises.

## Arithmetic

```python
print(10 + 3)
print(10 - 3)
print(10 * 3)
print(10 / 3)
print(10 // 3)
print(10 % 3)
print(10 ** 3)
```

## Assignment

```python
score = 10
score += 5
score *= 2
print(score)
```

## Comparison

```python
print(10 == 10)
print(10 != 3)
print(10 > 3)
print(10 <= 10)
```

## Logical

```python
age = 20
has_ticket = True

print(age >= 18 and has_ticket)
print(age < 18 or has_ticket)
print(not has_ticket)
```

## Identity

```python
first = None
second = None

print(first is second)
print(first is not second)
```

## Membership

```python
print("Python" in "Python programming")
print(3 in [1, 2, 3])
print("x" not in "text")
```

## Bitwise

```python
print(5 & 3)
print(5 | 3)
print(5 ^ 3)
print(5 << 1)
print(5 >> 1)
```

## Precedence

```python
print(2 + 3 * 4)
print((2 + 3) * 4)
print(2 ** 3 ** 2)
```

Use [operator precedence](precedence.md) for the complete evaluation order and precedence rules.

## Practical checklist

Before continuing, make sure you can:

- [ ] Use arithmetic operators correctly.
- [ ] Choose assignment operators that communicate intent.
- [ ] Build and combine comparisons.
- [ ] Use `and`, `or`, and `not` in conditions.
- [ ] Distinguish identity from value equality.
- [ ] Test membership in strings and collections.
- [ ] Understand and use bitwise operators.
- [ ] Predict expression evaluation using operator precedence.
