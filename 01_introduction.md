# Introduction

## What is Python?

https://www.python.org/doc/essays/blurb/

https://docs.python.org/3/faq/general.html

## Python 2 or Python 3


- The two versions are similar, with knowledge of one switching to writing code
for the other is easy.

- https://wiki.python.org/moin/Python2orPython3

    - The 2.x branch will see no new major releases after that. 3.x is under
active development [...] This means that all recent standard library
improvements, for example, are only available by default in Python 3.x.
    - Python ecosystem has amassed a significant amount of quality software over
the years. The downside of breaking backwards compatibility in 3.x is that some
of that software (especially in-house software in companies) still doesn't work
on 3.x yet.

## Installation

Windows doesn't come with Python, the installer and instructions can be found
https://docs.python.org/3/using/windows.html

Most \*nix based operating systems come with Python installed (usually Python
2). Replacing the system Python is not recommended and may cause problems.
However, different versions of Python can be safely installed along side the
system Python.

https://docs.python.org/3/using/index.html

-- Add instructions? ---
-- Mention Cloud9 IDE? --

## Python Interpreter

The Python interpreter is what is used to run Python scripts.

If it is available and in Unix shell’s search path makes it possible to start it
by typing the command `python` followed by the script name will invoke the
interpreter and run the script.

`hello_campers.py`
```python
if __name__ == '__main__':
    print('Hello campers!')
```
From terminal:
```
$ python hello_campers.py
Hello campers!
```

When multiple versions of Python are installed, calling them by version is
possible depending on the install configuration. In the Cloud9 ide custom
environment, they can be invoked like:

```
$ python --version
Python 2.7.6
$ python3 --version
Python 3.4.3
$ python3.5 --version
Python 3.5.1
```

## Python Interpreter Interactive Mode

Interactive mode can be started by invoking the Python interpreter with the `-i`
flag or without any arguments.

Interactive mode has a prompt where Python commands can be entered and run:

```
$ python3.5
Python 3.5.1 (default, Dec 18 2015, 00:00:00)
[GCC 4.8.4] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print("Hello campers!")
Hello campers!
>>> 1 + 2
3
>>> 3 * 4
12
>>> exit()
$
```

## The Zen of Python

Some of the principles that influenced the design of Python are included as an
easter egg and can be read by using the command:

```{.python .input  n=1}
import this
```

```{.json .output n=1}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "The Zen of Python, by Tim Peters\n\nBeautiful is better than ugly.\nExplicit is better than implicit.\nSimple is better than complex.\nComplex is better than complicated.\nFlat is better than nested.\nSparse is better than dense.\nReadability counts.\nSpecial cases aren't special enough to break the rules.\nAlthough practicality beats purity.\nErrors should never pass silently.\nUnless explicitly silenced.\nIn the face of ambiguity, refuse the temptation to guess.\nThere should be one-- and preferably only one --obvious way to do it.\nAlthough that way may not be obvious at first unless you're Dutch.\nNow is better than never.\nAlthough never is often better than *right* now.\nIf the implementation is hard to explain, it's a bad idea.\nIf the implementation is easy to explain, it may be a good idea.\nNamespaces are one honking great idea -- let's do more of those!\n"
 }
]
```

## Documentation

Python is well documented at https://docs.python.org/3/. The docs include
tutorials, guides, references and meta information for language.

Another important reference is the Python Enhancement Proposals (PEPs)
https://www.python.org/dev/peps/. Included in the PEPs is a style guide for
writing Python code, [`PEP 8`](https://www.python.org/dev/peps/pep-0008/).


## Debugging

Inline `print` statements can be used for simple debugging:

> **... often the quickest way to debug a program is to add a few print
statements to the source: the fast edit-test-debug cycle makes this simple
approach very effective.**

> [Executive Summary](https://www.python.org/doc/essays/blurb/)

Python also includes more powerful tools for debugging, such as:

* logging module, *logging*: https://docs.python.org/3/library/logging.html
* debugging module, *pdb*: https://docs.python.org/3/library/pdb.html

Just note that these exist for now.

## Hello World!

Going back to the docs, we can read about the `print` function, a [*built-in
function*](https://docs.python.org/3/library/functions.html) of the [Python
Standard Library](https://docs.python.org/3/library/index.html).

https://docs.python.org/3/library/functions.html#print

```
print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)
```

The built-in functions are listed in alphabetical order. The name is followed by
a parenthesized list of formal parameters with optional default values. Under
that is a short description of the function and its parameters are given and
occasionally an example.

The [`print`](https://docs.python.org/3/library/functions.html#print) function
in Python 3 replaces the
[`print`](https://docs.python.org/2/reference/simple_stmts.html#print) statement
in Python 2.

```{.python .input  n=2}
print("Hello world!")
```

```{.json .output n=2}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "Hello world!\n"
 }
]
```

A function is called when the name of the function is followed by `()`. For the
`Hello world!` example, the `print` function is called with a string as an
argument for the first parameter. For the rest of the parameters the defaults
are used.

The argument that we called the `print` function with is a `str` object or
*string*, one of Python's [*built-in
types*](https://docs.python.org/3/library/stdtypes.html#text-sequence-type-str).

The `objects` parameter is prefixed with a `*` which indicates that the function
will take an arbitrary number of arguments for that parameter.
