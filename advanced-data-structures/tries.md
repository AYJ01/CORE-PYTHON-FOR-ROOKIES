# Advanced Tries

A trie stores strings by their characters or prefixes. It is efficient for prefix matching and dictionary operations.

## Standard trie

```python
class TrieNode:
    def __init__(self):
        self.children = {}
        self.is_end = False


class Trie:
    def __init__(self):
        self.root = TrieNode()

    def insert(self, word):
        node = self.root
        for character in word:
            node = node.children.setdefault(character, TrieNode())
        node.is_end = True

    def search(self, word):
        node = self.root
        for character in word:
            node = node.children.get(character)
            if node is None:
                return False
        return node.is_end

    def starts_with(self, prefix):
        node = self.root
        for character in prefix:
            node = node.children.get(character)
            if node is None:
                return False
        return True
```

## Complexity

For a word of length `m`:

- Insert: O(m)
- Search: O(m)
- Prefix search: O(m)
- Storage: O(total characters × stored-node overhead)

## Variants

- Compressed trie / radix trie
- Suffix trie
- Suffix array for more compact storage
- Ternary search trie
- Aho-Corasick automaton for multiple pattern matching

## Exercises

1. Return every word matching a prefix.
2. Implement wildcard word search.
3. Find the longest common prefix.
4. Implement word break using trie nodes.
