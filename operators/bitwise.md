# Bitwise Operators

Bitwise operators work directly on the binary representation of integers.

| Operator | Meaning | Example |
|---|---|---|
| `&` | AND | `5 & 3` |
| `|` | OR | `5 | 3` |
| `^` | XOR | `5 ^ 3` |
| `~` | NOT / complement | `~5` |
| `<<` | Shift left | `5 << 1` |
| `>>` | Shift right | `5 >> 1` |

## Examples

```python
print(5 & 3)
print(5 | 3)
print(5 ^ 3)
print(~5)
print(5 << 1)
print(5 >> 1)
```

## Binary view

```python
print(bin(5))
print(bin(3))
print(bin(5 & 3))
print(bin(5 | 3))
print(bin(5 ^ 3))
```

## Common uses

Shift left multiplies positive integers by powers of two:

```python
print(1 << 3)
```

Shift right divides positive integers by powers of two:

```python
print(40 >> 3)
```

## Practical questions

1. Print `5 & 3`, `5 | 3`, and `5 ^ 3`.
2. Convert `10` and `12` to binary and find their AND result.
3. Multiply `7` by `8` using a left shift.
4. Divide `64` by `4` using a right shift.
5. Explain the result of `~0`.
