# Databases

Databases provide persistent storage and querying for application data.

## Navigation

- [Repository README](../README.md)
- [Databases](README.md)
- [SQLite basics](sqlite-basics.md)
- [Creating tables](creating-tables.md)
- [CRUD operations](crud-operations.md)
- [Parameterized queries](parameterized-queries.md)
- [Transactions](transactions.md)
- [Relationships](relationships.md)
- [Practical questions](practical-questions.md)

## Example

```python
import sqlite3

with sqlite3.connect("example.db") as connection:
    connection.execute(
        "CREATE TABLE IF NOT EXISTS users (id INTEGER PRIMARY KEY, name TEXT)"
    )
    connection.execute("INSERT INTO users (name) VALUES (?)", ("Asha",))

    print(connection.execute("SELECT * FROM users").fetchall())
```
