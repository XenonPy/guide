# XenonPy/guide
A guide that teaches you stuff
## Contents
* [Python Basics 1](Python-Basics-1)
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
> #### Versioning
> All examples for Python in this book were tested on Python `3.12`, however, they should work on any version of Python `3.9` or above.

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
But this is untidy. What if there were an easier way? Behold `f-strings`!
```python
language = "Python"
message = "Hello"

print(f"{language} {message}")
```
F-strings are the easiest way to include variables in strings, and they can actually include any expression. To make them, you simply declare the string as `f""` instead of `""` and add `{}` around any variables. Frontend programmers will recall that this also works in JSX. 

Now that you understand printing and variables, we can move on to **input**. Input is what makes your programs truly interactive, in fact, input is a part of almost all of the programs we use daily, in one form or another. Input is a **function** that returns a string. A function is just a name for a piece of reusable code that can take in any number of parameters (variables that you give to the function depending on what you're using it on), including none. It then executes code and optionally return a variable. Here's how to get input from the console:
```python
name = input("What is your name? ")
print(f"Hello {name}!")
```
Pretty simple, right? Just remember that if you don't include a space after your prompt (the string you have inside the parentheses), it might look a bit confusing. Prompts can also be `f-strings`, which makes them even more flexible.

So we can get input, print stuff, and store values. But we can't take actions based on them. That sounds like a job for **conditionals**! Conditionals are just if/else if/else statements. If you've ever seen a flowchart, conditionals are the progamming equivalent. Here's how to do a simple conditional:
