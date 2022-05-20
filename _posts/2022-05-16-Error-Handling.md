---
layout: post
title: Error Handling
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, error handling]
comments: true
---

### Errors

Obviously we have already encountered these before. Most of these can be identified directly by Python. Or through indicators assosciated with the error in question. Such as a `KeyError` or `ValueError`.

### Error Handling

For the most part, you don't want the end user to see these wacky error messages if there is a mistake in the code. Say you're looking to determine age and want to avoid accepting numbers into your program. Naturally, you can do it this way:

                `while True:
                    try:
                        age = int(input('what is your age? '))
                        print(age)
                    except ValueError:
                        print('please enter a number')
                    except ZeroDivisionError:
                        print('must be higher than zero')
                    else:
                        print('thank you!')
                        break`

The `except` feature here allows you to specify what kind of errors to look for. This allows you to categorize how you want your program to respond to errors. Especially since this program here uses these features to account for dividing by zero and when it recieves a string instead of an integer.

Good practice is to make `except` functions look for specific errors you might encounter with your program. Ones that might give you clues as to the solution.

### More Ways of Handling Errors

                `except (TypeError, ZeroDivisionError) as err:
                    print(err)

This summarizes the error and prints the string related to it. You can also attatch one function to multiple kinds of errors this way. Or add `as err` to have the individual errors display on command.

                except TypeError as err:
                    print(f'please enter numbers {err}')`

This one is triggered by a specific error.

Or:
                `except TypeError as err:
                    print(err)`

Same idea without `f-string`

### More While Loop Error Stuff

                `while True:
                    try:
                        age = int(input('whats your age? '))
                        10/age
                    except ValueError:
                        print('please enter a number')
                        continue
                    except ZeroDivisionError:
                        print('please enter age higher than 0')
                        break
                    else:
                        print('Thank you!')
                    finally:
                        print('Finally done!')
                    print('Can you hear me?')`

`raise` can be something you can add to the actual errors that come with the specific error you are awaiting.

                `while True:
                    try:
                        age = int(input('whats your age? '))
                        10/age
                        raise ValueError('Hey, cut that out!')`

This will then return the actual error with your own custom message printed with it.

You can run `Exception` and a message with the error will print out normally as well.
