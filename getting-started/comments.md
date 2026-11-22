# Comments

Comments explain code and are ignored by Python.

```python
# This is a comment
print("Hello")
```

## Multi-line comments

Python does not have a dedicated multi-line comment syntax. Use several `#` lines or a docstring for documentation:

```python
# Format a name.
# Add the title if supplied.
def format_name(name, title=""):
    """Return a formatted name."""
    return f"{title} {name}".strip()
```

Keep comments focused on why code exists when that purpose is not obvious.
