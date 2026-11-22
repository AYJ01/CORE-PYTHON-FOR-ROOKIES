# Networking

Networking lets Python programs exchange data across processes and machines. The standard library provides sockets for low-level communication and higher-level tools such as `http.client`, `urllib`, and `email` for common protocols.

## Navigation

- [Repository README](../README.md)
- [Networking](README.md)
- [Sockets](sockets.md)
- [HTTP](http.md)
- [APIs](apis.md)
- [Sockets and HTTP practical questions](practical-questions.md)

## Example

```python
from urllib.request import urlopen


with urlopen("https://example.com") as response:
    status = response.status
    body = response.read(100)

print(status)
print(body)
```
