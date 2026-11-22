<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/banner-light.svg">
  <img src="/banner-light.svg" alt="Python Tutorial for Beginners: learn Python 3 from first principles to professional systems" width="100%">
</picture>

<h1>Python Tutorial for Beginners: Learn Python 3</h1>

![Python](https://img.shields.io/badge/python-3.x-555555?style=flat-square&logo=python&logoColor=white&labelColor=2b2b2b)
![Level](https://img.shields.io/badge/level-beginner%20→%20advanced-555555?style=flat-square&labelColor=2b2b2b)
![Format](https://img.shields.io/badge/format-theory%20%2B%20practice-555555?style=flat-square&labelColor=2b2b2b)
![Status](https://img.shields.io/badge/status-active-555555?style=flat-square&labelColor=2b2b2b)

**A structured, hands-on Python 3 tutorial from first principles to professional-level systems.**

[Start learning](#learning-path) &nbsp;·&nbsp; [Theory notes](theory-notes/) &nbsp;·&nbsp; [Data structures](data-structures/) &nbsp;·&nbsp; [Advanced data structures](advanced-data-structures/) &nbsp;·&nbsp; [Practice projects](theory-notes/practice-and-projects.md) &nbsp;·&nbsp; [Contribute](#contributing)

<img src="assets/divider.svg" alt="" width="100%">

</div>

## Learn Python for beginners

`python-for-beginners` is a beginner-friendly Python learning system organized as a complete mastery path. It combines concise theory, runnable examples, practical exercises, and cross-topic projects. The lessons begin with installation and variables and progress through software design, testing, networking, concurrency, data structures, and advanced algorithms.

**Built for**

- New programmers taking their first steps
- Students learning Python through structured lessons
- Self-taught developers refreshing core concepts
- Learners progressing from fundamentals to architecture and concurrency
- Contributors who want small, focused educational pages

> [!NOTE]
> Read every page as a building block: understand the idea, predict the behavior, run the example, break it deliberately, and build a small project that combines the concept with earlier lessons.

## Learning path

| Stage | Topics | Skills gained |
|:--|:--|:--|
| **01 · Foundations** | [Getting Started](getting-started/) · [Variables](variables/) · [Operators](operators/) · [Strings](strings/) | Install Python, write and run programs, store values, manipulate text, evaluate expressions |
| **02 · Logic and Collections** | [Conditional Statements](conditional-statements/) · [Iterators](iterators/) · [Collections](collections/) · [Functions](functions/) | Make decisions, repeat work, organize information, reuse logic |
| **03 · Building Programs** | [Modules and Packages](modules-and-packages/) · [Virtual Environments](virtual-environments/) · [File Handling](file-handling/) · [Exception Handling](exception-handling/) · [Testing](testing/) | Organize projects, manage dependencies, save data, handle failures, verify behavior |
| **04 · Software Design** | [Object-Oriented Programming](object-oriented-programming/) · [Regular Expressions](regular-expressions/) · [Databases](databases/) · [Networking](networking/) | Model problems, process text, store information, communicate with APIs and services |
| **05 · Performance and Data** | [Data Structures](data-structures/) · [Concurrency](concurrency/) · [Advanced File Handling](advanced-file-handling/) · [Advanced Functions](advanced-functions/) · [Advanced OOP](advanced-object-oriented-programming/) | Choose appropriate structures and abstractions, process tasks, scale Python programs |
| **06 · Advanced Python** | [Advanced Data Structures](advanced-data-structures/) · [Advanced Modules](advanced-modules-and-packages/) · [Advanced Testing](advanced-testing/) · [Advanced Networking](advanced-networking/) · [Theory Notes](theory-notes/) | Analyze complex structures, package software, test systems, build network services |

> [!TIP]
> Follow the stages in order if you are new to Python. Experienced learners may enter at any topic, but every advanced section assumes familiarity with variables, functions, exceptions, modules, and testing. In `iterators/`, start with the `for` and `while` loop pages; generators and the iterator protocol can wait.

## Repository map

<details>
<summary><b>Show all 26 topic directories</b></summary>
<br>

```text
python-for-beginners/
├── getting-started/              Installation, execution, comments, first programs
├── variables/                    Values, names, types, conversions
├── operators/                    Arithmetic, logic, comparisons, precedence
├── strings/                      Creation, indexing, slicing, formatting, methods
├── conditional-statements/       if, elif, else, nesting
├── collections/                  Lists, tuples, sets, dictionaries
├── functions/                    Definitions, parameters, returns, scope, lambda
├── iterators/                    Loops, iterators, generators, protocols
├── modules-and-packages/         Imports, modules, packages, search paths
├── virtual-environments/         Isolation, activation, dependencies
├── file-handling/                Text, binary, CSV, JSON, paths
├── exception-handling/           try/except, custom exceptions, cleanup
├── testing/                      unittest, pytest, fixtures, mocking
├── object-oriented-programming/  Classes, inheritance, polymorphism
├── regular-expressions/          Pattern matching and text transformation
├── databases/                    SQLite, tables, CRUD, transactions
├── networking/                   Sockets, HTTP, APIs
├── concurrency/                  Threads, processes, asyncio, synchronization
├── data-structures/              Lists, stacks, queues, trees, graphs, heaps, hash tables
├── advanced-data-structures/     AVL and red-black trees, tries, segment trees, union-find,
│                                 caches, bloom filters, graph algorithms, and more
├── advanced-file-handling/       Archives, compression, locking, large files
├── advanced-functions/           Recursion, closures, decorators, annotations
├── advanced-object-oriented-programming/
│                                 Composition, ABCs, dataclasses, descriptors
├── advanced-modules-and-packages/
│                                 Internals, namespace packages, publishing
├── advanced-testing/             Coverage, doubles, async, property-based tests
├── advanced-networking/          TLS, protocols, async servers and clients
└── theory-notes/                 Detailed theory, glossary, learning and project guides
```

</details>

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

Depending on the operating system, use `python3 your_file.py` instead.

For project isolation:

```bash
python -m venv .venv
source .venv/bin/activate        # macOS/Linux
.venv\Scripts\activate           # Windows
python -m pip install --upgrade pip
```

No third-party runtime dependencies are required to study the core Markdown and standard-library examples.

## Learning resources

- [Theory overview](theory-notes/README.md)
- [Complete learning path](theory-notes/learning-path.md)
- [Directory-by-directory guide](theory-notes/directory-guide.md)
- [Python glossary](theory-notes/glossary.md)
- [Data structures tutorial](data-structures/README.md)
- [Advanced data structures tutorial](advanced-data-structures/README.md)
- [Practice and project ideas](theory-notes/practice-and-projects.md)

Each topic directory follows a consistent pattern:

- A focused `README.md` for navigation and an overview
- Dedicated Markdown pages for individual concepts
- Runnable Python examples
- A `practical-questions.md` exercise set
- Advanced follow-on concepts where the subject continues

## Example progression

### Level 1 · first program

```python
name = input("What is your name? ")
print(f"Hello, {name}! Welcome to Python.")
```

### Level 2 · decisions and collections

```python
scores = [72, 88, 91, 64]

for score in scores:
    if score >= 70:
        print(score, "passed")
    else:
        print(score, "needs practice")

print("Average:", sum(scores) / len(scores))
```

### Level 3 · reusable tested code

```python
from collections.abc import Iterable


def average(values: Iterable[float]) -> float:
    numbers = list(values)
    if not numbers:
        raise ValueError("at least one value is required")
    return sum(numbers) / len(numbers)


print(average([72, 88, 91, 64]))
```

### Level 4 · persistence and software structure

Combine `dataclasses`, functions, exception handling, SQLite, and tests to build a contact book or task tracker. Move data access behind small functions, validate input, use parameterized SQL, and test both successful and failure paths.

### Level 5 · data structures and algorithms

Explore [data structures](data-structures/) for lists, stacks, queues, trees, graphs, heaps, and hash tables. Continue with [advanced data structures](advanced-data-structures/) for balanced trees, tries, range structures, union-find, caches, and probabilistic structures.

## Learning tips

<details open>
<summary><b>Make predictions</b></summary>
<br>

Before running an example, write down what you expect it to print or return. Then compare the result. Prediction turns reading into active learning and makes debugging faster.

</details>

<details>
<summary><b>Use small experiments</b></summary>
<br>

Keep a playground file for unrelated experiments. Change one part at a time, and keep the successful version so that you can return to it.

</details>

<details>
<summary><b>Read errors from the end</b></summary>
<br>

Start with the final exception name and message, then use the traceback to locate the relevant line. A traceback is a chain of evidence, not a judgment about your ability.

</details>

<details>
<summary><b>Build progressively</b></summary>
<br>

Do not begin with a framework or a large application. Start with a calculator, quiz, guessing game, contact book, file processor, or simple server. Add features only after the basic version works.

</details>

<details>
<summary><b>Practice deliberately</b></summary>
<br>

Revisit a topic after a few days. Explain it in your own words, write an example without opening the lesson, solve the exercises, and apply it to a different problem.

</details>

## Project ladder

| # | Focus | Project ideas |
|:--:|:--|:--|
| 1 | Beginner | Greeter, calculator, quiz, number guessing game |
| 2 | Everyday Python | Shopping list, word analyzer, expense tracker |
| 3 | Files | Notes manager, CSV report, JSON settings tool |
| 4 | Databases | Contacts, inventory, task manager |
| 5 | Data structures | Stack-based undo, queue scheduler, trie, graph search |
| 6 | Object-oriented | Library catalog, game characters, banking system |
| 7 | Testing | Build every project addition test-first |
| 8 | Networking | API client, socket server, HTTP request tool |
| 9 | Advanced | Balanced search tree, range engine, cache, async service, reusable package |

Choose one or two of these projects instead of trying to learn every feature at once.

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

## Learning philosophy

Python mastery is not achieved by memorizing a language specification. It is the ability to translate a real problem into clear code, choose the right abstractions, verify behavior, recover from errors, and explain decisions.

> Learn slowly enough to understand. Build consistently enough to progress. Explain clearly enough to retain.

## License

See the [LICENSE](LICENSE) file for terms of use before copying or redistributing content.

<div align="center">

<img src="/divider.svg" alt="" width="100%">

<sub>Keep learning. Keep experimenting. Keep building.</sub>

</div>
