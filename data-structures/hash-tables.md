# Hash Tables and Dictionaries

A hash table maps keys to values using a hash function. Python dictionaries provide a highly optimized hash-table implementation.

## Theory

A key is passed through a hash function. The resulting value identifies a bucket. If multiple keys have the same bucket, a collision-resolution strategy is required.

Python commonly uses hash-based indexing and collision resolution internally. Dictionary keys must be hashable.

## Dictionary example

```python
inventory = {"apple": 12, "banana": 7}

inventory["apple"] = 15
inventory["orange"] = 20

print(inventory.get("pear", 0))
print(inventory)
```

## Custom hash table

```python
class HashTable:
    def __init__(self, size=10):
        self.buckets = [[] for _ in range(size)]

    def _bucket(self, key):
        return hash(key) % len(self.buckets)

    def put(self, key, value):
        bucket = self.buckets[self._bucket(key)]

        for index, (existing_key, _) in enumerate(bucket):
            if existing_key == key:
                bucket[index] = (key, value)
                return

        bucket.append((key, value))

    def get(self, key, default=None):
        bucket = self.buckets[self._bucket(key)]

        for existing_key, value in bucket:
            if existing_key == key:
                return value

        return default
```

## Complexity

| Operation | Average | Worst case |
|---|---:|---:|
| Insert | O(1) | O(n) |
| Search | O(1) | O(n) |
| Delete | O(1) | O(n) |

## Hashable values

Use immutable, stable values as keys:

```python
name_to_id = {"Ada": 1, "Lin": 2}
coordinates = {(10, 20): "point A"}
```

Avoid using mutable lists or sets as dictionary keys.
