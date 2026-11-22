# APIs

An API is an interface through which software components communicate. REST-style HTTP APIs commonly use JSON and resource URLs.

```python
import json
from urllib.request import urlopen


with urlopen("https://api.github.com/repos/python/cpython", timeout=10) as response:
    repository = json.load(response)

print(repository["full_name"])
print(repository["stargazers_count"])
```

## Best practices

- Send an appropriate `Accept` header.
- Authenticate securely with environment variables.
- Use rate limits and pagination correctly.
- Retry only after identifying transient failures.
- Never place secrets directly in source code.
