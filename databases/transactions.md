# Transactions

Transactions group database changes so they are committed together or rolled back if an error occurs.

```python
import sqlite3

connection = sqlite3.connect("example.db")
try:
    connection.execute("BEGIN")
    connection.execute("UPDATE accounts SET balance = balance - 100 WHERE id = 1")
    connection.execute("UPDATE accounts SET balance = balance + 100 WHERE id = 2")
    connection.commit()
except Exception:
    connection.rollback()
    raise
finally:
    connection.close()
```

The `with` form can simplify transaction handling:

```python
with sqlite3.connect("example.db") as connection:
    connection.execute("UPDATE accounts SET balance = balance - 100 WHERE id = 1")
    connection.execute("UPDATE accounts SET balance = balance + 100 WHERE id = 2")
```
