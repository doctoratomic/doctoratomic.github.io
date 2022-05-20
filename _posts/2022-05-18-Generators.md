---
layout: post
title: Generators
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, generators]
comments: true
---

### What are they?

They allow us to generate a sequence of values over time.

`range(100)` is a generator, it allows us to use a special keyword called `yield`.

Using `list(range(100))` will generate a series of numbers inside a list. And you can create a function that will help you adjust the list in any way you want.

                `def make_list(num):
                    result = []
                    for i in range(num):
                        result.append(i*2)
                    return result
                    
                my_list = make_list(100)
                print(my_list)`

This will make a function that multiplies each integer in the list by 2. And then saving it to the list before printing it's results.

Andre seems to imply that these lists are likely saved in temporary memory. And the more you try to generate, the more memory is taken up. There are more efficient ways to make large lists however. Outside of `print(list(range(10000000)))` that is.

### More Generator Stuff

Remember iterables?

Any objects in Python which you can loop through underneath the hood.

`Anything that is a generator is also iterable, but not everything that is iterable is a generator`

The `yield` function essentially turns your function into a generator variable. It pauses the function, and then waits for the `next` command to iterate to. It will recognize whether or not the range of numbers is adequate. And return the error of you input a limited range of numbers.

                `def generator_function(num):
                    for i in range(num):
                        yield i
                
                g = generator_function(1)
                next(g)
                next(g)
                print(next(g))
                
                print(next(g))`

Generators are great for calculating large sets of data. And useful for very long loops.

                `def gen_fun(num):
                    for i in range(num):
                        yield i
                        
                for item in gen_fun(100)`
