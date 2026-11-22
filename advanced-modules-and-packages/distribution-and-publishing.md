# Distribution and Publishing

Modern Python projects may use `pyproject.toml` to declare build metadata and dependencies.

```toml
[build-system]
requires = ["hatchling"]
build-backend = "hatchling.build"

[project]
name = "example-utilities"
version = "0.1.0"
description = "Small reusable Python utilities"
requires-python = ">=3.10"
```

## Build a package

```bash
python -m pip install --upgrade build twine
python -m build
```

## Install locally

```bash
python -m pip install -e .
```

Before publishing, test the package in an isolated environment and use trusted-package-index credentials. Verify package names and versions before uploading.
