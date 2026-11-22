# Custom Exceptions

Create application-specific exception types by subclassing `Exception` or a more specific built-in exception.

```python
class InsufficientFundsError(Exception):
    pass

class BankAccount:
    def __init__(self, balance):
        self.balance = balance

    def withdraw(self, amount):
        if amount > self.balance:
            raise InsufficientFundsError(
                f"Cannot withdraw {amount}; balance is {self.balance}"
            )
        self.balance -= amount
```

Usage:

```python
account = BankAccount(100)

try:
    account.withdraw(150)
except InsufficientFundsError as error:
    print(error)
```

Custom exceptions make domain failures easier to identify and handle.
