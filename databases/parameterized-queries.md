# Parameterized Queries

Always parameterize values supplied by callers or users.

```python
import sqlite3

name = input("Name: ")

with sqlite3.connect("example.db") as connection:
    rows = connection.execute(
        "SELECT id, name FROM users WHERE name = ?",
        (name,),
    ).fetchall()
```

Use SQL placeholders rather than string interpolation:

```python
# Unsafe: do not use for untrusted values
query = f"SELECT * FROM users WHERE name = '{name}'"
```

SQLite placeholders use `?` in the Python `sqlite3` module. Parameterized queries prevent values from being interpreted as SQL syntax.
