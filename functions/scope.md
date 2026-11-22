# Function Scope

## Local variables

```python
def example():
    message = "Local"
    print(message)

example()
```

`message` exists only inside `example()`.

## Global variables

```python
tax_rate = 0.18

def calculate_tax(amount):
    return amount * tax_rate

print(calculate_tax(100))
```

## Readable local variables

```python
def calculate_discount(price):
    discount = 0.10
    return price - (price * discount)
```

## The `global` keyword

Use `global` only when a function must intentionally update a module-level variable:

```python
counter = 0

def increment():
    global counter
    counter += 1

increment()
print(counter)
```

## The `nonlocal` keyword

`nonlocal` updates a variable in an enclosing function scope:

```python
def outer():
    count = 0

    def inner():
        nonlocal count
        count += 1

    inner()
    return count

print(outer())
