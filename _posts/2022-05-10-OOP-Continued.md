---
layout: post
title: OOP Continued
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, oop]
comments: true
---

### Super()

Allows you to refer to the parent class and it's attributes.

### Introspection

`dir` prints methods and attributes that the instance has access to!

Allows you to examine and test code before you finish

### Dunder Methods

"Magic Methods"

You can modify the function of these methods within classes.

Allows for full customization.

`__init__` & `__del__` are some examples of methods built into Python.

### MRO - Method Resolution Order

The order in which the computer reads the instances and it's parents.

                `class M(B,A,Z):
                    pass`

`__mro__` to check the order within your own code.

Helps define what order you will inherit in.
