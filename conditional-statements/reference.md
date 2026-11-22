# Conditional Statements Reference

## Navigation

- [Conditional statements](README.md)
- [If](if.md)
- [If-else](if-else.md)
- [Elif](elif.md)
- [Nested conditions](nested.md)
- [Practice](practical-questions.md)

## Syntax reference

```python
if condition:
    action()
elif another_condition:
    other_action()
else:
    fallback_action()
```

## Comparison checklist

| Need | Pattern |
|---|---|
| Single condition | `if condition:` |
| Two outcomes | `if ... else:` |
| Multiple outcomes | `if ... elif ... else:` |
| Decisions inside decisions | nested `if` blocks |
| One-line assignment | `value = x if condition else y` |

## Truth and falsy values

Falsy values include:

- `False`
- `None`
- `0`
- `0.0`
- `""`
- empty lists, tuples, dictionaries, and sets

Everything else is generally truthy.

```python
name = ""

if name:
    print("Name provided")
else:
    print("Name is missing")
```
