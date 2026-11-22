# SQLite Basics

SQLite stores an entire database in a local file and is included with Python.

```python
import sqlite3

connection = sqlite3.connect("example.db")
print(connection.execute("SELECT sqlite_version()").fetchone())
connection.close()
```

Use `with sqlite3.connect(...) as connection:` for connection-scoped resource handling. It does not necessarily close the connection at the end of the block; explicitly closing or using `contextlib.closing()` is useful when exact closure matters.
