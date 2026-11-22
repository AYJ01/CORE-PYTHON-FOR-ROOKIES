# Advanced Python Functions

Advanced function concepts support reusable, flexible, and maintainable Python code.

## Navigation

- [Repository README](../README.md)
- [Advanced Functions](README.md)
- [Recursion](recursion.md)
- [Closures](closures.md)
- [Decorators](decorators.md)
- [Higher-order functions](higher-order.md)
- [Function annotations](annotations.md)
- [Practical questions](practical-questions.md)

## Example

```python
def make_multiplier(factor):
    def multiply(value):
        return value * factor
    return multiply

double = make_multiplier(2)
triple = make_multiplier(3)

print(double(5))
print(triple(5))
```

This section introduces closures, decorators, recursion, higher-order functions, and annotations.
