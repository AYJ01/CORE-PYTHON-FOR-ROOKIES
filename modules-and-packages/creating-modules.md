# Creating Modules

A module is any `.py` file.

```python
# greetings.py

def hello(name):
    return f"Hello, {name}!"

def goodbye(name):
    return f"Goodbye, {name}!"
```

Import the module:

```python
import greetings

print(greetings.hello("Asha"))
print(greetings.goodbye("Asha"))
```

## Module entry point

```python
# greeting_app.py
import greetings

def main():
    print(greetings.hello("Python learner"))

if __name__ == "__main__":
    main()
```
