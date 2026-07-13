
<h1 align='center'>Introduction to Python</h1>

- [Introduction](#introduction)
- [Why Python?](#why-python)
    - [What Type of Language is Python?](#what-type-of-language-is-python)
- [Python Interactive Shell](#python-interactive-shell)
- [Comments](#comments)

## Introduction
Python is a general-purpose, high-level programming language known for its simple, English-like syntax. Python was created by a Dutch programmer, Guido van Rossum. The name '*Python*' was derived from **“Monty Python’s Flying Circus”** a British comedy show (though the snake 🐍 became the logo). The first version was released on February 20, 1991.

## Why Python?
Guido van Rossum had worked on ABC, a teaching language known for its clean, readable syntax but ABC was hard to extend and poorly integrated with operating systems and other tools. Python was essentially conceived as ABC's successor, keeping the clean, readable syntax but fixing ABC's extensibility and openness problems.  
Around the same period, other options had tradeoffs: C was fast but low-level and complex; C++ added OOP but was heavy, and scripting languages like Perl were messy.  
To overcome these issues, Guido van Rossum created Python: a simple, readable (like English), general-purpose, open-source, and extensible (can use C/C++ libraries) language.

### What Type of Language is Python?

- **High-level language** → closer to human language than machine code.
- **Interpreted** → executes line by line (no need for compilation).
- **General-purpose** → can be used for web, data science, AI, machine learning, automation, games, etc.
- **Dynamically typed** → no need to declare variable type explicitly.
- **Object-Oriented** → Everything is as an object in Python. Even functions, classes and modules.

## Python Interactive Shell
Python comes with a Python Interactive Shell. It is used to write and execute a single python command and get the result. To open the Python interactive shell, write **`python`** in your terminal or command prompt. Now you can write your command next to the '>>>' symbol.

```
>>> 5 + 10
15
>>> print("Hello World!")
Hello World!
```

Run **`import this`** in your terminal to checkout **The Zen of Python** i.e. everything that Python stands for.

```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```
Run `exit()` command to close the shell.

## Comments
Comments are the lines in the code that are ignored by the interpreter during the execution of the program. They enhance the readability of the code and allow developers to leave notes within their code.

1. **Single-line Comments:** In Python, single-line comment can be inline comment or can be written in new line. Anything followed by `#` is a single-line comment.

2. **Multi-line Comments:**  Multi-line comments are not available in python but we can achieve it by using triple-quoted string `'''...'''` or `"""..."""` if it is not assigned to a variable. They cannot be used as inline comments.   
Triple-quoted strings aren't actually comments — they're string literals. The interpreter doesn't ignore them the way it ignores `#` lines; it evaluates them as an expression statement and then discards the result (since nothing uses it).

```python
# This is single-line comment
print(2 + 3)   # 5 (Inline comment)

"""
This is multiline comment.
Multiline comment takes multiple lines.
"""
```
--- 
<p align="right">
    <a href="https://github.com/xerohit/Xero-to-Python/blob/main/01_Variables_&_Data_Types/01_Variables_&_Data_Types.md"><i>Variables & Data Types >></i></a>
</p>