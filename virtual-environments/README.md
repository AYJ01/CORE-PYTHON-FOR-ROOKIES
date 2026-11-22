# Virtual Environments

A virtual environment isolates a project's Python packages.

## Navigation

- [Repository README](../README.md)
- [Virtual Environments](README.md)
- [Why virtual environments](why.md)
- [Creating environments](creating.md)
- [Activating environments](activating.md)
- [Installing packages](installing-packages.md)
- [Requirements files](requirements.md)
- [Practical questions](practical-questions.md)

## Example

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install requests
python -m pip freeze > requirements.txt
```
