# CRUD Operations

CRUD means create, read, update, and delete data.

```python
import sqlite3

with sqlite3.connect("example.db") as connection:
    cursor = connection.execute(
        "INSERT INTO users (name, email) VALUES (?, ?)",
        ("Asha", "asha@example.com"),
    )
    user_id = cursor.lastrowid

    print(connection.execute("SELECT * FROM users WHERE id = ?", (user_id,)).fetchone())

    connection.execute("UPDATE users SET name = ? WHERE id = ?", ("Asha Rao", user_id))
    connection.execute("DELETE FROM users WHERE id = ?", (user_id,))
```

Transactions are committed or rolled back according to the SQLite connection's behavior. Be explicit about commit and rollback in application code.
