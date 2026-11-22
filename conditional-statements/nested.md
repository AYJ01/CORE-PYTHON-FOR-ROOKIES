# Nested Conditions

A nested condition is an `if`, `elif`, or `else` statement inside another conditional block.

## Example

```python
age = 20
has_ticket = True

if age >= 18:
    if has_ticket:
        print("Entry allowed")
    else:
        print("A ticket is required")
else:
    print("Must be 18 or older")
```

## Simplifying nested conditions

Sometimes logical operators produce clearer code:

```python
if age >= 18 and has_ticket:
    print("Entry allowed")
else:
    print("Entry denied")
```

Use nesting when each level has distinct decisions.

## Example: sign and range

```python
number = 15

if number >= 0:
    if 10 <= number <= 20:
        print("Positive and between 10 and 20")
    else:
        print("Positive, outside the range")
else:
    print("Negative")
```

## Practical questions

1. Check whether a number is positive and even.
2. Allow a purchase only if the buyer is logged in and has enough balance.
3. Classify a character as uppercase, lowercase, or neither.
4. Check whether a student passed and earned an award.
5. Decide whether a user can access an admin page based on login and role.
