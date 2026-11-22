# CORE-PYTHON-FOR-ROOKIES

<div align="center">

![Python](https://img.shields.io/badge/Python-3-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-4CAF50?style=for-the-badge)
![Format](https://img.shields.io/badge/Format-Theory%20%2B%20Practice-FF9800?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-2196F3?style=for-the-badge)

**A structured, hands-on Python curriculum from first principles to professional-level systems.**

[Start learning](#learning-path) · [Theory notes](theory-notes/) · [Practice projects](theory-notes/practice-and-projects.md) · [Contribute](#contributing)

</div>

---

## About this repository

`CORE-PYTHON-FOR-ROOKIES` is a beginner-friendly Python learning system organized as a complete mastery path. It combines concise theory, runnable examples, practical exercises, cross-topic projects, and expanded advanced material.

The repository is designed for:

- New programmers taking their first steps
- Students learning Python through structured lessons
- Self-taught developers refreshing core concepts
- Learners progressing from fundamentals to architecture and concurrency
- Contributors who want small, focused educational pages

Read every page as a building block: understand the idea, predict the behavior, run the example, break it deliberately, and build a small project that combines the concept with earlier lessons.

---

## Learning path

| Stage | Topics | Skills gained |
|:---|:---|:---|
| **01 — Foundations** | [Getting Started](getting-started/) · [Variables](variables/) · [Operators](operators/) · [Strings](strings/) | Install Python, write and run programs, store values, use types, work with text, and evaluate expressions |
| **02 — Logic and Collections** | [Conditional Statements](conditional-statements/) · [Collections](collections/) · [Functions](functions/) · [Iterators](iterators/) | Make decisions, organize data, reuse logic, repeat work, and understand iteration |
| **03 — Building Programs** | [Modules and Packages](modules-and-packages/) · [Virtual Environments](virtual-environments/) · [File Handling](file-handling/) · [Exception Handling](exception-handling/) · [Testing](testing/) | Split projects into modules, isolate dependencies, persist data, handle failures, and verify behavior |
| **04 — Software Design** | [Object-Oriented Programming](object-oriented-programming/) · [Regular Expressions](regular-expressions/) · [Databases](databases/) · [Networking](networking/) | Model domain concepts, process text, query persistent data, and communicate over a network |
| **05 — Performance and Scale** | [Concurrency](concurrency/) · [Advanced File Handling](advanced-file-handling/) · [Advanced Functions](advanced-functions/) · [Advanced OOP](advanced-object-oriented-programming/) | Design reusable abstractions and work efficiently with asynchronous tasks, large files, and advanced language features |
| **06 — Professional Python** | [Advanced Modules](advanced-modules-and-packages/) · [Advanced Testing](advanced-testing/) · [Advanced Networking](advanced-networking/) · [Theory Notes](theory-notes/) | Package and distribute software, test complex systems, build resilient network services, and connect the complete curriculum |

> Follow the stages in order if you are new to Python. Experienced learners may enter at any topic, but every advanced section assumes familiarity with variables, functions, exceptions, modules, and testing.

---

## Repository map

```text
CORE-PYTHON-FOR-ROOKIES/
├── getting-started/              Installation, execution, comments, first programs
├── variables/                    Values, names, types, conversions
├── operators/                    Arithmetic, logic, comparisons, precedence
├── strings/                      Creation, indexing, slicing, formatting, methods
├── conditional-statements/      if, elif, else, nesting
├── collections/                 Lists, tuples, sets, dictionaries
├── functions/                   Definitions, parameters, returns, scope, lambda
├── iterators/                    Loops, iterators, generators, protocols
├── modules-and-packages/         Imports, modules, packages, search paths
├── virtual-environments/         Isolation, activation, dependencies
├── file-handling/                Text, binary, CSV, JSON, paths
├── exception-handling/           try/except, custom exceptions, cleanup
├── testing/                      unittest, pytest, fixtures, mocking
├── object-oriented-programming/ Classes, inheritance, polymorphism
├── regular-expressions/         Pattern matching and text transformation
├── databases/                   SQLite, tables, CRUD, transactions
├── networking/                  Sockets, HTTP, APIs
├── concurrency/                 Threads, processes, asyncio, synchronization
├── advanced-file-handling/       Archives, compression, locking, large files
├── advanced-functions/          Recursion, closures, decorators, annotations
├── advanced-object-oriented-programming/
│                               Composition, ABCs, dataclasses, descriptors
├── advanced-modules-and-packages/
│                               Internals, namespace packages, publishing
├── advanced-testing/            Coverage, doubles, async, property-based tests
├── advanced-networking/         TLS, protocols, async servers and clients
└── theory-notes/                Detailed theory, glossary, learning and project guides
```

---

## Recommended use

### Beginner workflow

1. Choose one topic from the learning path.
2. Open the topic `README.md` and read the subpages in sequence.
3. Predict the output of every example before running it.
4. Type the code instead of copying and pasting.
5. Complete the practical questions.
6. Change values and deliberately introduce one error at a time.
7. Build the smallest project that uses the completed concept.

### Mastery loop

```text
Learn → Predict → Implement → Test → Debug → Explain → Extend
```

Ask yourself:

- What problem does this concept solve?
- What is the simplest working example?
- What breaks when invalid or unexpected input is provided?
- How does this work with variables, collections, functions, files, and tests?
- Can I explain it clearly without reading the page?

### Running an example

Python 3 is required.

```bash
python your_file.py
```

Depending on the operating system, use:

```bash
python3 your_file.py
```

For project isolation:

```bash
python -m venv .venv
source .venv/bin/activate        # macOS/Linux
.venv\Scripts\activate           # Windows
python -m pip install --upgrade pip
```

No third-party runtime dependencies are required to study the core Markdown and standard-library examples.

---

## Learning resources

- [Theory overview](theory-notes/README.md)
- [Complete learning path](theory-notes/learning-path.md)
- [Directory-by-directory guide](theory-notes/directory-guide.md)
- [Python glossary](theory-notes/glossary.md)
- [Practice and project ideas](theory-notes/practice-and-projects.md)

Each topic directory follows a consistent pattern:

- A focused `README.md` for navigation and an overview
- Dedicated Markdown pages for individual concepts
- Runnable Python examples
- A `practical-questions.md` exercise set
- Advanced follow-on concepts where the subject continues

---

## Example progression

### Level 1 — first program

```python
name = input("What is your name? ")
print(f"Hello, {name}! Welcome to Python.")
```

### Level 2 — decisions and collections

```python
scores = [72, 88, 91, 64]

for score in scores:
    if score >= 70:
        print(score, "passed")
    else:
        print(score, "needs practice")

print("Average:", sum(scores) / len(scores))
```

### Level 3 — reusable tested code

```python
from collections.abc import Iterable


def average(values: Iterable[float]) -> float:
    numbers = list(values)
    if not numbers:
        raise ValueError("at least one value is required")
    return sum(numbers) / len(numbers)


print(average([72, 88, 91, 64]))
```

### Level 4 — persistence and software structure

Combine `dataclasses`, functions, exception handling, SQLite, and tests to build a contact book or task tracker. Move data access behind small functions, validate input, use parameterized SQL, and test both successful and failure scenarios.

---

## Learning tips

<details open>
<summary><strong>Make predictions</strong></summary>

Before running an example, write down what you expect it to print or return. Then compare the result. Prediction turns reading into active learning and makes debugging faster.

</details>

<details>
<summary><strong>Use small experiments</strong></summary>

Keep a playground file for unrelated experiments. Change one part at a time, and keep the successful version so that you can return to it.

</details>

<details>
<summary><strong>Read errors from the end</strong></summary>

Start with the final exception name and message, then use the traceback to locate the relevant line. A traceback is a chain of evidence, not a judgment about your ability.

</details>

<details>
<summary><strong>Build progressively</strong></summary>

Do not begin with a framework or a large application. Start with a calculator, quiz, guessing game, contact book, file processor, or simple server. Add features only after the basic version works and is tested.

</details>

<details>
<summary><strong>Practice deliberately</strong></summary>

Revisit a topic after a few days. Explain it in your own words, write an example without opening the lesson, solve the exercises, and apply it to a different problem.

</details>

---

## Project ladder

1. **Beginner:** greeter, calculator, quiz, or number guessing game
2. **Everyday Python:** shopping list, word analyzer, expense tracker
3. **Files:** notes manager, CSV report, JSON settings tool
4. **Databases:** contacts, inventory, or task manager
5. **Object-oriented:** library catalog, game characters, banking system
6. **Testing:** build every project addition test-first
7. **Networking:** API client, socket server, or HTTP request tool
8. **Advanced:** async service, protocol parser, reusable package, or plugin system

Choose one or two of these projects instead of trying to learn every feature at once.

---

## Contributing

Contributions should preserve clarity and educational quality.

- Keep examples compatible with Python 3
- Explain unfamiliar terms in plain language
- Include a runnable example and a practical exercise when appropriate
- Use descriptive file and directory names
- Avoid secrets, real credentials, unsafe commands, or external private data
- Test code before submitting it
- Update navigation links and README indexes when changing structure
- Keep advanced pages separate from beginner introductions

Open an issue or pull request with a short description of the improvement. Small fixes are welcome.

---

## Learning philosophy

Python mastery is not achieved by memorizing a language specification. It is the ability to translate a real problem into clear code, choose the right abstractions, verify behavior, recover from errors, and improve the design through testing and review.

> Learn slowly enough to understand. Build consistently enough to progress. Explain clearly enough to retain.

---

## License

Check the repository for license information before copying or redistributing content.

<div align="center">

**Keep learning. Keep experimenting. Keep building.**

</div>
