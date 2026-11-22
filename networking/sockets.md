# Sockets

A socket is an endpoint for network communication. TCP provides a reliable, ordered byte stream; UDP provides datagrams without guaranteed delivery or ordering.

## TCP client

```python
import socket


with socket.create_connection(("example.com", 80)) as connection:
    connection.sendall(b"GET / HTTP/1.1\r\nHost: example.com\r\nConnection: close\r\n\r\n")
    response = connection.recv(4096)

print(response.decode("utf-8", errors="replace"))
```

## TCP server

```python
import socket


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as server:
    server.bind(("127.0.0.1", 8080))
    server.listen()

    connection, address = server.accept()
    with connection:
        print("Connected by", address)
        connection.sendall(b"Hello, client!")
```
