# Creating Tables

Create tables with SQL `CREATE TABLE` statements.

```python
import sqlite3

with sqlite3.connect("example.db") as connection:
    connection.execute(
        """
        CREATE TABLE IF NOT EXISTS users (
            id INTEGER PRIMARY KEY,
            name TEXT NOT NULL,
            email TEXT NOT NULL UNIQUE
        )
        """
    )
```

Choose constraints that enforce valid application data:

- `PRIMARY KEY`
- `NOT NULL`
- `UNIQUE`
- `CHECK`
- `DEFAULT`
