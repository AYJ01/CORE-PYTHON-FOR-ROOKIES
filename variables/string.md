# String Variables

A string (`str`) stores text such as names, messages, and sentences.

```python
name = "Asha"
greeting = 'Hello'
message = "Python is fun!"
```

Use matching quotation marks around a string. Triple quotes can represent multi-line text:

```python
poem = """Rows of data,
Lines of code,
Python in motion."""
```

## String operations

Concatenation joins strings:

```python
first = "Ada"
last = "Lovelace"
full_name = first + " " + last
print(full_name)
```

Repetition repeats a string:

```python
print("*" * 10)
```

## f-strings

F-strings insert variable values and expressions:

```python
name = "Sam"
age = 20
print(f"{name} is {age} years old.")
```

## Useful string methods

```python
text = "  Python Notes  "

print(text.strip())
print(text.upper())
print(text.lower())
print(text.replace("Notes", "Guide"))
print(text.count("o"))
```

Methods do not usually modify the original string; strings are immutable.

## Indexing and slicing

```python
word = "Python"
print(word[0])
print(word[-1])
print(word[:3])
print(word[3:])
```

## Escaped characters

```python
print("She said, \"Hello!\"")
print("Name\tScore")
print("First line\nSecond line")
```

## String length

```python
code = "PYTHON"
print(len(code))
```

## Converting to string

```python
value = 100
text = str(value)
print(text + " points")
```

## Practical questions

1. Create `first_name` and `last_name`, combine them, and print the full name.
2. Convert `"python programming"` to title case.
3. Remove spaces from both ends of `"  Hello  "`.
4. Print the first and last characters of `"Rookie"`.
5. Use an f-string to print `"Maria has 3 books"` from two variables.
