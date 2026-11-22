# Identity Operators

Identity operators test whether two variables refer to the same object.

| Operator | Meaning | Example |
|---|---|---|
| `is` | Both names refer to the same object | `value is None` |
| `is not` | Names refer to different objects | `value is not None` |

## Identity versus equality

```python
left = [1, 2, 3]
right = [1, 2, 3]

print(left == right)
print(left is right)

right = left
print(left is right)
```

Use `==` to compare values. Use `is` to compare object identity.

## Checking for None

```python
value = None

if value is None:
    print("No value")

if value is not None:
    print("Value exists")
```

## Practical questions

1. Create two separate lists with identical values; compare `==` and `is`.
2. Assign one list to another name and check their identity.
3. Create a variable set to `None`; check it with `is`.
4. Explain the difference between identity and equality.
5. Write code that rejects a `None` value.
