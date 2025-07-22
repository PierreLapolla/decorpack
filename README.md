# Decorpack

[![PyPI](https://img.shields.io/pypi/v/decorpack)](https://pypi.org/project/decorpack/)  
[![CI](https://github.com/PierreLapolla/decorpack/actions/workflows/publish.yml/badge.svg)](https://github.com/your‑org/decorpack/actions)

A small collection of reusable Python decorators and utilities for logging, timing, singletons, and safe‑exception handling.

## Features
 
- `logger`: pre-configured Python logger ready to use 
- `singleton`: decorator  and metaclass for enforcing single-instance class
- `timer`: decorator to measure function runtime 
- `try_except`: decorator for catching & handling exceptions cleanly

## Installation

```bash
  pip install decorpack
```

## Quickstart

```python
from decorpack import timer, singleton, log, try_except


@timer
def expensive_computation(x):
    pass


@singleton
class MyConfig:
    pass


@try_except(ValueError)
def parse_int(s: str) -> int:
    return int(s)


log.info("Quickstart over!")
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
