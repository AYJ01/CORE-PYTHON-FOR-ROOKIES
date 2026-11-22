# HTTP

HTTP is an application protocol for transferring resources. Each request uses a method such as `GET`, `POST`, `PUT`, or `DELETE`, and receives a response containing a status code, headers, and an optional body.

```python
from urllib.request import Request, urlopen


request = Request(
    "https://httpbin.org/post",
    data=b'{"message":"hello"}',
    headers={"Content-Type": "application/json"},
    method="POST",
)

with urlopen(request, timeout=10) as response:
    print(response.status)
    print(response.read().decode())
```

HTTP headers describe metadata, status codes indicate outcomes, and JSON is a common response format. Use timeouts and handle network, HTTP, and decoding errors in real applications.
