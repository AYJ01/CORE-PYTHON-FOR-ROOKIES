# LRU and LFU Caches

A cache keeps frequently used or recently used values in limited memory.

## LRU cache

An LRU (least recently used) cache removes the value that has gone unused the longest.

```python
from collections import OrderedDict


class LRUCache:
    def __init__(self, capacity):
        if capacity <= 0:
            raise ValueError("capacity must be positive")
        self.capacity = capacity
        self.values = OrderedDict()

    def get(self, key):
        if key not in self.values:
            return None

        value = self.values.pop(key)
        self.values[key] = value
        return value

    def put(self, key, value):
        if key in self.values:
            self.values.pop(key)

        self.values[key] = value

        if len(self.values) > self.capacity:
            self.values.popitem(last=False)


cache = LRUCache(2)
cache.put("A", 1)
cache.put("B", 2)
print(cache.get("A"))
cache.put("C", 3)
print(cache.get("B"))
```

## LFU cache

An LFU (least frequently used) cache removes the item with the smallest access frequency.

Implementation needs a dictionary for values and frequencies, plus collections of keys at each frequency. This allows O(1) average get and put operations.

## Comparison

| Policy | Good for | Weakness |
|---|---|---|
| LRU | Recent-access workloads | Ignores long-term popularity |
| LFU | Stable, popular items | Old popular items may dominate |
| FIFO | Simple operational limits | No usage-awareness |

## Exercises

1. Implement LFU using frequency buckets.
2. Add a TTL expiration timestamp.
3. Track cache-hit and cache-miss statistics.
4. Compare LRU behavior against FIFO for a workload.
