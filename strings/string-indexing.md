# String Indexing

Each character in a string has a position, beginning at zero.

```python
text = "Python"

print(text[0])
print(text[1])
print(text[-1])
```

Output:

```text
P
y
n
Strings are immutable. Assigning to an index raises an error:

```python
text[0] = "J"
```
