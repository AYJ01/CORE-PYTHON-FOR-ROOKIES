# Learning Path: from first steps to confident Python

This path is a suggestion, not a race. Move on when you can explain the basic idea in your own words and try a small example. If a later topic feels confusing, go back to the earlier folder it builds on.

## Trail 1: meet Python

### 1. Getting started

Open [`getting-started/`](../getting-started/README.md). Learn what Python is, how to install and run it, how to use the interactive prompt, and how to write a first program. A program is simply a set of instructions the computer follows. Try `print("Hello!")` and then change the message.

### 2. Variables and values

Open [`variables/`](../variables/README.md). A variable is a name attached to a value, like a labeled box: `score = 10`. Learn numbers (`integer.md`, `float.md`), text (`string.md`), true/false values (`boolean.md`), and changing values from one type to another (`type-conversion.md`).

### 3. Operators

Open [`operators/`](../operators/README.md). Operators are symbols or words that do work with values: add with `+`, compare with `>`, combine conditions with `and`. Learn arithmetic before bitwise operators; bitwise work is an optional, more technical part of this folder.

### 4. Decisions

Open [`conditional-statements/`](../conditional-statements/README.md). An `if` statement is like a choice: “if it is raining, take an umbrella; otherwise, take sunglasses.” Learn `if`, `if-else`, `elif`, and nested choices. Conditions use ideas from variables and comparison operators.

### 5. Text and groups of things

Read [`strings/`](../strings/README.md), then [`collections/`](../collections/README.md). Strings are text; lists, tuples, sets, and dictionaries organize multiple values. Think of a list as an ordered row of boxes, a set as a collection that keeps only one of each value, and a dictionary as labeled information such as a contact card.

### 6. Reusable actions

Open [`functions/`](../functions/README.md). A function is a named recipe: give it inputs, let it do steps, and it may give back an answer. Learn how to define functions, use parameters, return values, and understand scope. Try writing a function that converts minutes to seconds.

## Trail 2: make programs do more

### 7. Loops and iteration

Open [`iterators/`](../iterators/README.md). Loops repeat work. A `for` loop visits items one at a time; a `while` loop continues while a condition is true. Later pages explain iterators and generators, which produce values one at a time.

### 8. Organize code and protect it from mistakes

Study [`modules-and-packages/`](../modules-and-packages/README.md) to split code into reusable files. Study [`exception-handling/`](../exception-handling/README.md) to respond thoughtfully when something goes wrong. Then learn [`testing/`](../testing/README.md): tests are small checks that help you know whether code behaves as intended.

### 9. Save information

Read [`file-handling/`](../file-handling/README.md) to read and write files, use paths, and work with CSV and JSON. Then explore [`databases/`](../databases/README.md) to store information in SQLite tables and find it again with queries. Use parameterized queries rather than joining user text into SQL.

### 10. Keep project tools tidy

Use [`virtual-environments/`](../virtual-environments/README.md) to give a project its own package space. A virtual environment is like a separate toolbox for one project, so its installed tools do not accidentally mix with another project's tools.

## Trail 3: design and deeper ideas

### 11. Objects and advanced functions

Begin with [`object-oriented-programming/`](../object-oriented-programming/README.md): classes are plans for creating objects that hold information and actions. Continue with [`advanced-object-oriented-programming/`](../advanced-object-oriented-programming/README.md) for composition, data classes, context managers, and other deeper tools. Read [`advanced-functions/`](../advanced-functions/README.md) for recursion, closures, decorators, higher-order functions, and annotations after ordinary functions feel comfortable.

### 12. Text patterns and communication

[`regular-expressions/`](../regular-expressions/README.md) teaches patterns for finding or changing text. [`networking/`](../networking/README.md) introduces internet addresses, sockets, HTTP, and APIs. Read [`advanced-networking/`](../advanced-networking/README.md) later for TLS, asynchronous connections, and protocol design. Do not send private information to a website you do not trust.

### 13. Speed, large files, and stronger checks

[`concurrency/`](../concurrency/README.md) compares threads, processes, and asyncio for tasks that overlap. [`advanced-file-handling/`](../advanced-file-handling/README.md) covers large files, temporary files, archives, compression, and locking. [`advanced-testing/`](../advanced-testing/README.md) expands testing with coverage, integration, async, and property-based tests. [`advanced-modules-and-packages/`](../advanced-modules-and-packages/README.md) explores package initialization and distribution.

## Checkpoints

Before moving to the next trail, see if you can:

- Explain the idea without copying the page's words.
- Write a tiny example from memory, then check it against the lesson.
- Change an example and predict how the output changes.
- Find the relevant page again when you forget a detail.

If not yet, repeat the lesson or ask a question. Repeating is how learning works.
