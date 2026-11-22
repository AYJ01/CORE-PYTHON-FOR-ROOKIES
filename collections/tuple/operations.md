# Tuple Operations

## Concatenation and repetition

```python
left = (1, 2)
right = (3, 4)

print(left + right)
print(left * 3)
```

## Membership

```python
colors = ("red", "green", "blue")

print("green" in colors)
print("yellow" not in colors)
```

## Iteration and unpacking

```python
for color in colors:
    print(color)

point = (10, 20)
x, y = point
print(x, y)
```

## Nested tuples

```python
matrix = ((1, 2), (3, 4))
print(matrix[0][1])
```
