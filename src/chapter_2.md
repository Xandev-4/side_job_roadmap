# 01. Python

Priority: **Core** = learn first, **Next** = after Core / when a project needs it, **Later** = just know it exists.

## A. Basics

| Done | Concept                                                                  | Priority | What you should be able to do                  |
| ---- | ------------------------------------------------------------------------ | -------- | ---------------------------------------------- |
| ☐    | Running Python, REPL, scripts                                            | Core     | Run a `.py` file and use the interactive shell |
| ☐    | Variables, naming, dynamic typing                                        | Core     | Explain what a variable actually points to     |
| ☐    | Data types: int, float, str, bool, None                                  | Core     | Convert between types, spot type errors        |
| ☐    | Operators (arithmetic, comparison, logical, `in`, `is`)                  | Core     | Know `==` vs `is`                              |
| ☐    | Input / output, f-strings, `print` formatting                            | Core     | Build clean output                             |
| ☐    | Conditionals (`if/elif/else`)                                            | Core     | Write branching logic                          |
| ☐    | Loops (`for`, `while`, `break`, `continue`, `range`, `enumerate`, `zip`) | Core     | Loop over anything without index tricks        |
| ☐    | Functions (args, kwargs, defaults, return, scope)                        | Core     | Split a script into small functions            |
| ☐    | Mutable vs immutable, references                                         | Core     | Explain why a list changes inside a function   |

## B. Built-in data structures

| Done | Concept                                            | Priority | What you should be able to do                  |
| ---- | -------------------------------------------------- | -------- | ---------------------------------------------- |
| ☐    | Lists (indexing, slicing, methods, sorting)        | Core     | Use `append`, `pop`, `sort`, `sorted`, slicing |
| ☐    | Tuples and unpacking                               | Core     | Swap, return multiple values                   |
| ☐    | Sets (union, intersection, membership)             | Core     | Remove duplicates, check membership fast       |
| ☐    | Dictionaries (get, items, setdefault, iteration)   | Core     | Count things, group things                     |
| ☐    | Strings (methods, slicing, split/join, formatting) | Core     | Parse and clean text                           |
| ☐    | List / dict / set comprehensions                   | Core     | Replace simple loops with comprehensions       |
| ☐    | `collections` (Counter, defaultdict, deque)        | Next     | Use them in DSA problems                       |
| ☐    | `itertools`, `functools` basics                    | Later    | Know they exist                                |

## C. Files, errors, modules

| Done | Concept                                                                     | Priority | What you should be able to do                    |
| ---- | --------------------------------------------------------------------------- | -------- | ------------------------------------------------ |
| ☐    | Reading / writing text files, `with` statement                              | Core     | Save and load data                               |
| ☐    | JSON and CSV modules                                                        | Core     | Read/write structured data                       |
| ☐    | Exceptions (`try/except/else/finally`, raising)                             | Core     | Handle bad input without crashing                |
| ☐    | Modules and imports, `if __name__ == "__main__"`                            | Core     | Split code into multiple files                   |
| ☐    | `pip`, virtual environments (`venv`), `requirements.txt`                    | Core     | Set up a clean env per project                   |
| ☐    | Standard library tour (`os`, `pathlib`, `datetime`, `random`, `math`, `re`) | Core     | Know what's available before installing packages |
| ☐    | Regular expressions (`re`)                                                  | Next     | Extract patterns from text                       |

## D. OOP

| Done | Concept                                                     | Priority | What you should be able to do         |
| ---- | ----------------------------------------------------------- | -------- | ------------------------------------- |
| ☐    | Classes, objects, `__init__`, `self`                        | Next     | Model a real thing (User, Task)       |
| ☐    | Instance vs class attributes, methods                       | Next     | Explain the difference                |
| ☐    | Inheritance, `super()`, method overriding                   | Next     | Extend a base class                   |
| ☐    | Dunder methods (`__str__`, `__repr__`, `__eq__`, `__len__`) | Next     | Make objects print and compare nicely |
| ☐    | `@property`, `@staticmethod`, `@classmethod`                | Next     | Know when each fits                   |
| ☐    | Encapsulation, composition vs inheritance                   | Next     | Choose composition when it fits       |
| ☐    | Abstract base classes, protocols                            | Later    | Know the idea                         |

## E. Intermediate Python

| Done | Concept                                               | Priority | What you should be able to do                    |
| ---- | ----------------------------------------------------- | -------- | ------------------------------------------------ |
| ☐    | Type hints                                            | Next     | Annotate functions and read other people's hints |
| ☐    | `dataclasses`                                         | Next     | Replace boilerplate classes                      |
| ☐    | Pydantic (models, validation)                         | Next     | Validate data (you'll use this in FastAPI)       |
| ☐    | Iterators and generators (`yield`)                    | Next     | Process data lazily                              |
| ☐    | Decorators                                            | Next     | Write a simple timer or logger decorator         |
| ☐    | Context managers (custom `with`)                      | Next     | Know how `with` works under the hood             |
| ☐    | `*args`, `**kwargs`, lambda, `map/filter`             | Next     | Read and write them                              |
| ☐    | `async` / `await`, `asyncio` basics                   | Next     | Understand why FastAPI uses it                   |
| ☐    | Logging module                                        | Next     | Replace `print` debugging in projects            |
| ☐    | Environment variables (`os.environ`, `python-dotenv`) | Next     | Keep secrets out of code                         |
| ☐    | Working with APIs (`requests` / `httpx`)              | Next     | Call a public API and parse the result           |

## F. Quality and tooling

| Done | Concept                                             | Priority | What you should be able to do  |
| ---- | --------------------------------------------------- | -------- | ------------------------------ |
| ☐    | Debugging (reading tracebacks, `pdb`, IDE debugger) | Core     | Find a bug without guessing    |
| ☐    | Testing with `pytest`                               | Next     | Write tests for pure functions |
| ☐    | Code style (PEP 8), `ruff` / `black`                | Next     | Keep code clean automatically  |
| ☐    | Project structure (packages, `__init__.py`)         | Next     | Organise a multi-file project  |
| ☐    | `pyproject.toml`, `uv` / `poetry`                   | Later    | Know modern packaging          |

## G. Deeper Python

| Done | Concept                               | Priority | What you should be able to do |
| ---- | ------------------------------------- | -------- | ----------------------------- |
| ☐    | Threading vs multiprocessing, the GIL | Later    | Explain when each helps       |
| ☐    | Memory model, garbage collection      | Later    | Know it exists                |
| ☐    | Metaclasses, descriptors              | Later    | Skip for now                  |
| ☐    | C extensions, performance tuning      | Later    | Skip for now                  |

## Mini-projects to prove you know it

- [ ] CLI to-do app that saves to a JSON file
- [ ] Text file analyser (word counts, most common words)
- [ ] Simple quiz or flashcards game
- [ ] Script that calls a public API and prints a clean report
- [ ] A small class-based project (library system, bank account)
