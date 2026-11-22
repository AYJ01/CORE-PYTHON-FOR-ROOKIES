# Closures

A closure is a function that retains access to variables from an enclosing scope.

```python
def make_greeting(greeting):
    def greet(name):
        return f"{greeting}, {name}!"

    return greet

hello = make_greeting("Hello")
welcome = make_greeting("Welcome")

print(hello("Asha"))
print(welcome("Ben"))
```

## Counter closure

```python
def make_counter(start=0):
    count = start

    def increment():
        nonlocal count
        count += 1
        return count

    return increment

counter = make_counter()
print(counter())
print(counter())
```

Closures remember state even after the enclosing function has returned.
