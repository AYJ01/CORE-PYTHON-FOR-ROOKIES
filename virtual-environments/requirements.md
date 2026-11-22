# Requirements Files

Create a `requirements.txt` file:

```bash
python -m pip freeze > requirements.txt
```

Install dependencies from it:

```bash
python -m pip install -r requirements.txt
```

Pin versions only for dependencies where reproducibility matters. For production projects, separate direct dependencies from fully resolved versions where appropriate.
