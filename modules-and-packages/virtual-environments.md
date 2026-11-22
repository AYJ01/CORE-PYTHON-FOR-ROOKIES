# Virtual Environments

A virtual environment isolates project dependencies.

## Create and activate

```bash
python -m venv .venv
```

Windows activation:

```bash
.venv\Scripts\activate
```

Linux and macOS activation:

```bash
source .venv/bin/activate
```

## Install dependencies

```bash
python -m pip install requests
```

List or freeze dependencies:

```bash
python -m pip list
python -m pip freeze > requirements.txt
```

Always use `python -m pip` so packages are installed for the active Python interpreter.
