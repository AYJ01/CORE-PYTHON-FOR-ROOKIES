# Advanced Modules and Packages Practical Questions

1. Create lightweight package initialization code.
2. Re-export public APIs with `__all__`.
3. Define a namespace package.
4. Combine namespace packages from multiple directories.
5. Import a module dynamically.
6. Reload a module safely.
7. Inspect `sys.modules`.
8. Print module metadata attributes.
9. Detect circular imports.
10. Replace relative imports correctly.
11. Design a plugin discovery mechanism.
12. Protect plugin loading with validation.
13. Add `pyproject.toml` to a package.
14. Build a wheel and source distribution.
15. Install a package in editable mode.
16. Add package metadata and dependencies.
17. Create an isolated test environment.
18. Publish a test release to a test package index.
19. Test imports after installation.
20. Document the package's public API.

## Mini-project

Create a plugin-based text-processing package. Support namespace-package plugins discovered at runtime, expose a stable public API, and package the project with `pyproject.toml`. Include at least one built-in plugin and one independently importable plugin.
