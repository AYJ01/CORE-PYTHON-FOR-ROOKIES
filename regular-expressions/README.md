# Regular Expressions

Regular expressions (regex) describe patterns in text. Python provides the `re` module for searching, matching, splitting, and replacing text.

## Navigation

- [Repository README](../README.md)
- [Regular Expressions](README.md)
- [Basic patterns](basic-patterns.md)
- [Groups and capturing](groups-and-capturing.md)
- [Search and replace](search-and-replace.md)
- [Flags and compilation](flags-and-compilation.md)
- [Lookarounds](lookarounds.md)
- [Practical questions](practical-questions.md)

## Basic example

```python
import re

text = "Contact: support@example.com"
match = re.search(r"[\w.-]+@[\w.-]+\.[A-Za-z]{2,}", text)

if match:
    print(match.group())
```
