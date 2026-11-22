# TLS

TLS encrypts network traffic and authenticates servers through certificates. Python SSL sockets validate certificates and host names by default when using secure-context helpers.

```python
import socket
import ssl


context = ssl.create_default_context()
with socket.create_connection(("example.com", 443)) as raw_socket:
    with context.wrap_socket(raw_socket, server_hostname="example.com") as tls_socket:
        tls_socket.sendall(b"GET / HTTP/1.1\r\nHost: example.com\r\nConnection: close\r\n\r\n")
        print(tls_socket.recv(4096).decode("utf-8", errors="replace"))
```

## Security

- Keep certificate verification enabled.
- Use modern protocol and cipher defaults.
- Restrict which CA certificates a context trusts when appropriate.
- Store private keys securely and never commit them.
