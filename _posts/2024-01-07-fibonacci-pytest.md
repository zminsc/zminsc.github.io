---
title: fibonacci pytest
layout: article
---

I was first introduced to the concept of test-driven-development (TDD) in CIS 1200, the introductory programming course at Penn. The course was taught in OCaml and Java; unit tests were written with an OCaml Assert module and the JUnit library respectively. Bored over winter break, I decided I would figure out how to write unit tests in Python. My main concern: how difficult would the whole thing be to set up and use?

The answer: not as difficult as I was expecting. After watching the first thirty minutes of [this](https://www.youtube.com/watch?v=43mwW9IEo8M) YouTube video, I booted up Visual Studio Code, opened a new folder, and created a Python virtual environment. Next, I executed `pip install pytest` in the terminal to install **pytest**, a Python unit-testing framework. I then created two files: **fibonacci.py** and **test_fibonacci.py**; the latter would store my unit tests. Important note: all tests written in **test_fibonacci.py** must be prepended by `test_`.

**fibonacci.py**:

```python
def get_fibonacci(n):
    if n == 0:
        return 0
    if n == 1 or n == 2:
        return 1
    return get_fibonacci(n - 1) + get_fibonacci(n - 2)
```

**test_fibonacci.py**:

```python
from fibonacci import get_fibonacci

def test_get_fibonacci_zero():
    assert get_fibonacci(0) == 0

def test_get_fibonacci_one():
    assert get_fibonacci(1) == 1

def test_get_fibonacci_two():
    assert get_fibonacci(2) == 1

def test_get_fibonacci_three():
    assert get_fibonacci(3) == 2

def test_get_fibonacci_ten():
    assert get_fibonacci(10) == 55
```

Simply executing `pytest` in the terminal executes all the unit tests. I have yet to figure out benchmarking and code coverage, but this will do for now.
