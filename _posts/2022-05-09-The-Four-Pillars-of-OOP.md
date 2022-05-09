---
layout: post
title: The Four Pillars of OOP
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, oop]
comments: true
---

### Encapsulation

The binding of data and functions that manipulate the data. That becomes encapsulated to one big object. Keeping everything in essentially a box that other developers and programs can interact with.

I suppose in the simplest of terms, it is the idea of the internal logic of each function you create. Each class, object, method, all being contained in one simple object.

While it is an advanced concept, it is merely a method of structuring your own custom logic within the program.

### Abstraction

Hiding of information, giving access to only what's necessary.

An idea of keeping things simple. You know what you need to know.

### Private vs. Public Variables

Related to abstraction.

There are no true `private variables` in Python. You must indicate in some way with your code that these variables must not be changed.

Using double underscores (__) on both sides of the variable (`__name__`) is a common way to indicate these variables are private. And Python methods can easily be overwritten if your naming conventions are not careful enough.

### Inheritance

Allows new objects to take on the properties of existing objects.

Inherit classes.

The example: showing off how a game could potentially organize it's online users.

                `"""
                Players for game

                """

                class User:
                 def sign_in(self):
                  print('logged in!')

                class Wizard(User):
                 def __init__(self, name, level):
                  self.name = name
                  self.level = level

                 def attack(self):
                  print(f'attacking with power of {self.level}')

                class Knight(User):
                def __init__(self, name, level):
                  self.name = name
                  self.level = level

                def attack():
                  print(f'attacking with power of {self.level}')

                wizard1 = Wizard('Cornelius', 15)
                knight1 = Knight('Arthur', 25)

                knight1.attack()`

All of these classes operate under the umbrella of the `User` class. Hypothetically confirming that the classes are players in the game.

### Polymorhpism

Allows us to have many forms.

Allows you to essentially form a hierarchy of custom data based on certain parameters and organizes it accordingly.

A concept borrowed from biology where an organism or species can have many different forms or stages.
