# Set Operations

## Membership

```python
languages = {"Python", "Java", "Rust"}
print("Python" in languages)
```

Sets are ideal for fast membership tests, but they do not support indexing or slicing.

## Iteration

```python
for language in languages:
    print(language)
```

## Mathematical operations

```python
python_users = {"Asha", "Ben", "Chen"}
rust_users = {"Ben", "Deepa", "Eve"}

print(python_users | rust_users)
print(python_users & rust_users)
print(python_users - rust_users)
print(python_users ^ rust_users)
```

- `|`: union
- `&`: intersection
- `-`: difference
- `^`: symmetric difference
