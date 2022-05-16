---
layout: post
title: Functional Programming
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, functional programming]
comments: true
---

### What is it?

It's all about seperation of concerns. Which OOP does as well.

It's about packaging code into chunks so that it's organized in a way that makes sense.

Based on functionality.

Each part concerns itself with one thing that it does really well.

Boils down to some basic principles of writing code.

* The code is clear and understandable

* Easy to extend or expand upon

* Easy to maintain

* Memory Efficient

* DRY (Not repeating!)

### Pure Functions

There is an idea that there's a seperation between data of a program and it's behaviour.

Always produces the same output, regardless of input.

There are no side effects. Everything is self contained. Unaffecting the global scope.

### map()

Allows us to simplify functions

                `def multiply_by2(item):
                    return item*2
                    
                print(list(map(multiply_by2, [1,2,3])))`

`map` calls the function for us. Data `[1,2,3]` gets acted upon `multiply_by2`. Purifying the function to the point where we don't need to add much else. As it supplies both the data and the function.

This is also effectifly a way to loop through data.

Creating a list outside of this function can also be called in the function like `print(list(map(multiply_by2, my_list)))`

This will create a new list automatically, and still retain the original list. As it is immutable.

### filter()

                `my_list = [1,2,3]
                def multiply_by2(item):
                    return item*2
                
                def only_odd(item):
                    return item % 2 != 0
                    
                print(list(filter(only_odd, my_list)))`

`%` gives the remainder of the number. Since it is `2`, the function is looking to filter out even numbers with the `!= 0`

`filter` effectively filters out data based on the function. In this case, we are determining whether the numbers in the list are divisible by 2. And returning those that are not.

Returning `[1,3]`

### zip()

                `my_list = [1,2,3]
                your_list = [10,20,30]
                def multiply_by2(item):
                    return item*2
                
                def only_odd(item):
                    return item % 2 != 0
                    
                print(list(zip(my_list, your_list)))`

`zip` outputs a combination of the two lists. Adding the first in each list together in a tuple `(1,10)`. This is done regardless of what kind of lists we use. `zip` will always return the combined list this way `[(1,10), (2,20), (3,30)]`. You can even add to the individual tuples the more data structures you want to combine.

Can be very useful due to the utility and generic nature of this function.

### reduce()

A bit advanced [git gud]

`from functools import reduce` this is the first time Andre has even brought up this "advanced" topic.

My general understanding, is that despite the extensive functions that come with Python, you can import custom ones from the internet.

I am familiar with this already, as you have to learn how to use the console to make sure Python can read them correctly.

                `from functools import reduce
                my_list = [1,2,3]
              
                def multiply_by2(item):
                    return item*2
                
                def only_odd(item):
                    return item % 2 != 0
                
                def accumulator(acc, item):
                    return acc + item
                    
                print(list(reduce(accumulator,my_list, 0)))`

`reduce` loops through the function and takes two parameters. The `acc` and the `item` it recieves.

Adding `10` in place of zero would return the following.

                `10 0
                11 1
                13 2
                16 3`

### Lambda Expressions

One time anonymous functions (no name / label attatched to them.)

Good for functions you only need to run once.

`print(list(map(lambda item: item*2, my_list)))`

Makes code less readable to others, but simplifies the code as well

### List Comprehensions

`my_list = [char for char in 'hello']`

`my_list2 = [num for num in  range(0,1000)]`

This is a faster way of creating lists. Including ones that have a range of numbers. You can also do these things with `sets` and `dictionaries` as well!

## Set and Dictionary Comprehensions

`set = {}` these only allow unique items.

                `dictionaries = {
                    'a': 1,
                    'b': 6
                }`

To create a comprehension for a dictionary, the syntax will look like this:

`my_dict = {k:v**2 for k,v in dictionaries.items() if v%2==0}`

While this may be harder to read. This definetly makes for simpler code.

The list is taking the `key` which is the string value in the dictionary, and multiplying the `value` or the integers in the dictionary by the power of 2. Iterates over the dictionary and checks to see if it is divisible by 2. And adds it to the dictionary.
