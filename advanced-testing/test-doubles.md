# Test Doubles

Test doubles include stubs, fakes, mocks, and spies. Choose the smallest replacement that isolates the behavior under test.

## Stub

```python
class WeatherClientStub:
    def get_temperature(self):
        return 21
```

## Fake

```python
class UserRepositoryFake:
    def __init__(self):
        self.users = {}

    def save(self, user):
        self.users[user["id"]] = user

    def get(self, user_id):
        return self.users.get(user_id)
```

## Mock

```python
from unittest.mock import Mock

notifier = Mock()
notifier.send("done")
notifier.send.assert_called_once_with("done")
```

Prefer a fake for a stateful subsystem and a mock only when interaction verification is the point of the test.
