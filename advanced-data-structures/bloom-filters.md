# Bloom Filters

A Bloom filter is a probabilistic set structure. It reports:

- `definitely absent` for an item not inserted
- `probably present` for an item believed to be inserted

It never creates false negatives, but may create false positives.

## Implementation

```python
import hashlib


class BloomFilter:
    def __init__(self, bit_count, hash_count):
        self.bits = [False] * bit_count
        self.hash_count = hash_count

    def _positions(self, item):
        first = int(hashlib.md5(str(item).encode()).hexdigest(), 16)
        second = int(hashlib.sha1(str(item).encode()).hexdigest(), 16)

        for index in range(self.hash_count):
            yield (first + index * second) % len(self.bits)

    def add(self, item):
        for position in self._positions(item):
            self.bits[position] = True

    def contains(self, item):
        return all(self.bits[position] for position in self._positions(item))


bloom = BloomFilter(1000, 5)
bloom.add("python")
print(bloom.contains("python"))
print(bloom.contains("java"))
```

## Sizing

For `n` inserted elements and desired false-positive probability `p`:

```text
bit_count ≈ -(n * ln(p)) / (ln(2)²)
hash_count ≈ (bit_count / n) * ln(2)
```

## Uses

- Web cache screening
- Database block filtering
- Distributed membership checks
- Spell-checking or content deduplication pipelines

## Trade-offs

- Fast membership tests
- Compact memory usage
- No enumeration
- No standard deletion support
- False positives affect exact applications
