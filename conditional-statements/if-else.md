# If-Else Statements

An `if-else` statement chooses one of two code paths.

## Basic syntax

```python
age = 16

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

## Example: pass or fail

```python
score = 45

if score >= 50:
    print("Pass")
else:
    print("Fail")
```

## Example: positive or negative

```python
number = -4

if number >= 0:
    print("Non-negative")
else:
    print("Negative")
```

## Ternary conditional expression

For simple assignments, Python provides a concise conditional expression:

```python
age = 20
status = "Adult" if age >= 18 else "Minor"
print(status)
```

Prefer a normal `if-else` block when the code is complex.

## Practical questions

1. Print `"Even"` or `"Odd"` for a number.
2. Print `"Pass"` or `"Fail"` for a score.
3. Choose `"High"` or `"Low"` for a temperature.
4. Choose `"Available"` or `"Unavailable"` for stock.
5. Assign `"Over"` or `"Within"` based on a budget.
