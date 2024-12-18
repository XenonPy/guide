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
lastVariable = 2.9
```
Variables in Python can be declared as above. They can contain `a-Z`, `0-9`, and `_`, but they must not start with a number or underscore, and they may not end with an underscore.
> Note: Leading underscores have vaild use cases for names, such as internal functions in modules, and trailing underscores are used in some `builtin` methods, but for now stick to the above rules.

But what can we do with these variables? The next thing to learn is printing. First let's discuss the two **data types** we've learned so far. We have:

| Name  | Value | Example |
| ------------- | ------------- | ----- |
| Integer  | A whole number  | `y = 45`|
| String  | Text  | `name = "XenonPy`   |
| Float | A decimal number | `x = 5.3`|

Note that some types are compatible, and others are not. Here's how to print to the console:

```python
y = 52
language = "Python"
x = 97.4
message = "Hello"
z = 3

print(y)
print(x)
print(x + y)
print(language)
print(message + language)
print(message * 3)
```
> If you're confused about the symbols, math in python is `*` for multiplication, `/` for division, `+` for addition, and `-` for subtraction. There are other special ones you'll learn about later.

The output is:
```
52
97.4
149.4
Python
HelloPython
HelloHelloHello
```
Let's go over what this means. The first four work as we'd expect. Adding strings is a bit weird, but reasonable. But multiplying a string gives an interesting result: it repeats the string that many times. Say we want to print `"Hello Python"` without adding spaces to our variables. Here's the first way:
```python
language = "Python"
message = "Hello"

print(language + " " + message)
```
But this is untidy. What if there were an easier way? Behold `f-strings`.
```python
language = "Python"
message = "Hello"

print(language + " " + message)
```
