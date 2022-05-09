---
layout: post
title: Object Oriented Programming
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning]
comments: true
---

### What is OOP?

Classes are the data types like `booleans` and `floats` and `integers`

Every one of these things can be considered an `object`

You can use methods on said objects with the `DOT '.'` method. This is so you can perform actions on them. Like `.find` or `.upper`.

OOP essentially allows you to create your own data types WITHIN Python.

IT IS A WAY OF THINKING

IT IS A PARADIGM

Programming started out as procedural code. Which was code that was read from top to bottom.

Using `class` can allow one to create a new Data type.

                `class BruceWayne:
                pass`

Object Oriented Programming, is really ideas about `Objects` and `classes` and their relationship to one another.

A `class` is like a blueprint.

You make a `class` to then `instantiate` new `instances` which are all objects.

Instantiating a class would essentially look like this:

                `b_wayne = BruceWayne()`

### Creating Our Own Objects

                `class PlayerChar:
                    def __init__(self, name):
                    self.name = name
    
                    def run(self):
                        print('run')

                player1 = PlayerChar("Bimmy")
                print(player1.name)`

First: note the nature of the class naming `PlayerChar`. Two caps.

`__init__` is a special method (magic method/dunder method) Often called constructor method or init method. This is always called when you instantiate an object.

`self` refers to the player character. Or the object is referencing itself.

The parameter being used here is `name`. Which then becomes an object and can print the specific reference to that point in the data. Readable perhaps, much like a dictionary. Except you can program functions within these dictionaries.

### Attributes and Methods

Attributes are essentially `self.name = name`.

In a way it is a means of referencing itself when accessing the data within the class. `self` has become a placeholder for whatever you name the variable you assign to it. Like the last lines of the previous example. Using `.name` we can grab the attribute within that class to access the data in the object.

**Class Object Attributes**, are static not dynamic. Variables that remain constant within an object.

While **Attributes or Class Attributes** are dynamic. They are specific to each individual object.

### "init" or Constructor Methods

Instantiation is clearly an important part of OOP.

This allows you to specify and organize massive amounts of data down to a T.

                `class PlayerChar:
                    def __init__(self, name='Player', age='0'):
                    self.name = name
                    self.age = age

Adding default parameters and if statements to this class allows you to essentially create templates for organizing data.

### @classmethod

`@classmethod` is a way of creating methods inside of a class without instantiating it.

                `@classmethod
                def adding_things(cls, num1, num2):
                    return num1 + num2
                
                print(PlayerChar.adding_things(2,3))`

This technique isn't used as often. But it can come in handy in some cases.

`@staticmethod` works the same way as a class method. But you cannot use `cls` or the class itself.

We use static methods when we don't care about the state of the class. Or the attributes.

We use class methods when we do care, and we want to change the methods retroactively.

### Review

*Object oriented programming is a paradigm. Or a way of thinking in terms of structuring code.

*Went from writing procedural functions to things like OOP.

*We use classes to incorporate OOP paradigms.

*Create classes in Python with camelcase naming system. Tells other programmers that this is a class that gets instantiated.

*`__init__` is run on every instantiation to customize our objects.

*Using methods helps specify parameters and details important to the class. And that every method has access to the class.

*There are `class methods` and `static methods`, these can actually be called without instantiation.

