# Stacks in Python

A stack is a Last-In, First-Out (LIFO) structure. The latest item added is the first item removed.

## Operations

- `push`: add an item
- `pop`: remove and return the top item
- `peek`: inspect the top item
- `is_empty`: test whether the stack has items

## Implementation

```python
class Stack:
    def __init__(self):
        self._items = []

    def push(self, value):
        self._items.append(value)

    def pop(self):
        if self.is_empty():
            raise IndexError("pop from empty stack")
        return self._items.pop()

    def peek(self):
        if self.is_empty():
            raise IndexError("peek from empty stack")
        return self._items[-1]

    def is_empty(self):
        return len(self._items) == 0


stack = Stack()
stack.push("first")
stack.push("second")
print(stack.peek())
print(stack.pop())
```

## Complexity

All core stack operations are O(1).

## Uses

- Undo/redo operations
- Function call management
- Expression parsing
- Balanced-parentheses checks
- Browser history navigation
- Depth-first search

## Exercise: balanced brackets

```python
def balanced(text):
    pairs = {")": "(", "]": "[", "}": "{"}
    stack = []

    for character in text:
        if character in "([{":
            stack.append(character)
        elif character in pairs:
            if not stack or stack.pop() != pairs[character]:
                return False

    return not stack

print(balanced("([{}])"))
print(balanced("([)]"))
```
