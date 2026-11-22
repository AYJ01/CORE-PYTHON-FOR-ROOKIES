# Assignment Operators

Assignment operators store or update values in variables.

| Operator | Meaning | Example | Equivalent to |
|---|---|---|---|
| `=` | Assign | `x = 5` | `x = 5` |
| `+=` | Add and assign | `x += 3` | `x = x + 3` |
| `-=` | Subtract and assign | `x -= 3` | `x = x - 3` |
| `*=` | Multiply and assign | `x *= 3` | `x = x * 3` |
| `/=` | Divide and assign | `x /= 3` | `x = x / 3` |
| `//=` | Floor divide and assign | `x //= 3` | `x = x // 3` |
| `%=` | Remainder and assign | `x %= 3` | `x = x % 3` |
| `**=` | Exponentiate and assign | `x **= 3` | `x = x ** 3` |

## Updating a variable

```python
score = 10
score += 5
score *= 2
print(score)
```

## Multiple assignment

```python
left, right = 10, 20
left, right = right, left
print(left, right)
```

## Chained assignment

```python
a = b = c = 0
print(a, b, c)
```

## Augmented assignment

Augmented assignment reads the current value, applies an operator, and stores the result:

```python
count = 0
count += 1
count += 1
print(count)
```

## Practical questions

1. Start with `balance = 100`, add `25`, subtract `10`, and print the result.
2. Double a score variable using `*= 2`.
3. Assign `x`, `y`, and `z` in one statement.
4. Swap two variables using tuple assignment.
5. Use `+=` in a loop to add ten numbers.
