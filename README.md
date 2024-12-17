# XenonPy/guide
A guide that teaches you stuff
## Contents
* Python Basics 1
  * Estimated Time: 35 minutes
  * Skill Summary: Basic Python skills, including conditionals, functions, lists, dictionaries, and programming concepts
  * Project: Store Manager
* Web Basics 1
  * Estimated Time: 25 mins
  * Skill Summary: Understanding the different parts of a site, including HTML, CSS, and JS, and learning how to Inspect.
  * Project: Wiki
* Web Basics 2 
  * Estimated Time: 5 mins
  * Skill Summary: Understanding headers, URL parameters, and routes.
  * Project: CTF #1 (A little something to get you started)
* Working with the Shell
  * Estimated Time: 15 mins
  * Skill Summary: Learn how to manipulate files and run commands in a shell.
* Red Teaming 1: CTF
  * Estimated Time: 20 mins
  * Skill Summary: Complete your first hack! Learn how to use important tools and simple injection to exploit a site.
  * Project: CTF #2 (Micro-CMS v1)

# Python Basics 1
Python is the most used scripting language in the world. It's a powerful and versatile language, however, like most interpreted languages, it is slow in comparison to languages like C or Rust.
> ### Compiled vs Interpreted
> Compiled and Interpreted refer to how a language's code is run.
> Computers can't understand programming languages that we use.
> In compiled languages, like C, you run a compile step on your code which turns it into an executable that your OS can run directly.
> In intepreted languages, like Python, you can think of it as the compile step being run for each line at a time. This is why the following code will work:
> ```python
> x = "Hello"
> print(x)
> ```
> But this will not:
> ```python
> print(x)
> x = "Hello"
> ```
The first thing to learn in Python is variables. These are simply assigning a specific "name" that stores a specific value, so that you don't have to repeat yourself in your code.
```python
myVariable = "something"
anotherVariable = 65
```
Variables in Python can be declared as above. They can contain `a-Z`, `0-9`, and `_`, but they must not start with a number or underscore, and they may not end with an underscore.
> Note: this does not apply to builtin variables like `__name__`, and you may sometimes get away with it, but it it *highly* discouraged.

