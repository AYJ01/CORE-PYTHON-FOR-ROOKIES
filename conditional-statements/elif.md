# Elif Statements

Use `elif` to test multiple conditions in sequence.

## Basic syntax

```python
score = 72

if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
elif score >= 60:
    print("D")
else:
    print("F")
```

Only the first matching branch runs.

## Example: temperature categories

```python
temperature = 12

if temperature > 30:
    print("Hot")
elif temperature > 20:
    print("Warm")
elif temperature > 10:
    print("Cool")
else:
    print("Cold")
```

## Example: role selection

```python
role = "admin"

if role == "admin":
    print("Full access")
elif role == "editor":
    print("Edit access")
elif role == "viewer":
    print("Read-only access")
else:
    print("Unknown role")
```

## Practical questions

1. Convert a numeric score to A, B, C, D, or F.
2. Categorize a temperature as hot, warm, cool, or cold.
3. Convert traffic-light names into actions.
4. Assign fee tiers based on age.
5. Print a different message for beginner, intermediate, and advanced levels.
