# Operator Precedence

Operator precedence determines the order in which expressions are evaluated.

```python
print(2 + 3 * 4)
print((2 + 3) * 4)
```

Multiplication is evaluated before addition.

## Precedence table

Operators are shown from highest to lowest precedence.

| Rank | Operators |
|---|---|
| 1 | `( )` |
| 2 | `**` |
| 3 | `+x`, `-x`, `~x` |
| 4 | `*`, `/`, `//`, `%` |
| 5 | `+`, `-` |
| 6 | `<<`, `>>` |
| 7 | `&` |
| 8 | `^` |
| 9 | `|` |
| 10 | Comparisons: `==`, `!=`, `>`, `>=`, `<`, `<=`, `is`, `is not`, `in`, `not in` |
| 11 | `not` |
| 12 | `and` |
| 13 | `or` |

## Associativity

Most operators are evaluated left-to-right:

```python
print(20 / 5 * 2)
print(20 - 5 - 3)
```

Exponentiation is right-to-left:

```python
print(2 ** 3 ** 2)
print((2 ** 3) ** 2)
```

## Readable expressions

Prefer parentheses when an expression is complex:

```python
final_score = (base_score + bonus) * multiplier
is_valid = age >= 18 and (has_ticket or is_staff)
```

## Practical questions

1. Predict `10 + 4 * 3` before running it.
2. Compare `10 - 3 - 2` with `10 - (3 - 2)`.
3. Evaluate `2 ** 3 * 4`.
4. Parenthesize `age >= 18 and has_ticket or is_staff` clearly.
5. Rewrite a complex expression into smaller named values.
