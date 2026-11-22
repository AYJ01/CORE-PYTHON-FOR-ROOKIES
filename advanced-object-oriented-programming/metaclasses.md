# Metaclasses

A metaclass customizes class creation. Classes are instances of metaclasses, with `type` as the default metaclass.

```python
class RequiredMethods(type):
    def __new__(metaclass, name, bases, namespace):
        required = ("execute",)
        for method_name in required:
            if method_name not in namespace:
                raise TypeError(f"Missing method: {method_name}")
        return super().__new__(metaclass, name, bases, namespace)

class Job(metaclass=RequiredMethods):
    def execute(self):
        print("Executing")
```

Metaclasses are powerful but should be used only when decorator-based or normal OOP solutions are insufficient.
