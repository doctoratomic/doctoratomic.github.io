---
layout: post
title: Decorators
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, decorators]
comments: true
---

### What are Decorators

`@classmethod` & `@staticmethod` are just a few examples.

Functions are first class citizens, and act just like variables.

                `def hello():
                print(heelllllllooooo);
                
                greet = hello
                del hello
                
                print(greet)`

To summarize: the `del` function will delete all references to `hello` in memory. But `greet` is still attatched to the value that was inside the `hello` function.

Therefore, after you call the `hello()` function again once it's been deleted. It will not exist.

This is an important concept to understand regarding decorators.

### Higher Order or HOC

A function that accepts another function as a parameter.

ie:

                `def greet(func):
                    func()`

or:
                `def greet2():
                    def func():
                        return 5
                    return func`

It returns a function.


### Decorators, finally

A decorator supercharges a function. It is a function that wraps another function and enhances it.

                `def my_decorator(func):
                    def wrap_func():
                        print('***********')
                        func()
                        print('***********')
                    return wrap_func
                    
                @my_decorator
                def hello():
                    print('HELLO')
                    
                @my_decorator
                def bye():
                    print('Hasta la vista, baby')`

This allows you to essentially print functions within other functions. In this case, the code adds a visual flare to our greetings.


### Decorators Part 3 - The Decorating

Coming Soon!