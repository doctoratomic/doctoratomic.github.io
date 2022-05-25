---
layout: post
title: Debugging
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, debugging]
comments: true
---

### Principles

Debugging is a skill among many senior developers.

`Linting` = allows us to detect issues as one codes. IDE's like PyCharm or VSCode help with this.

`IDE/Editor` = choosing a specific editor can help in the process for debugging.

`Recognizing Errors` = knowing the difference between a `SyntaxError` and a `TypeError`.

### PDB

`Python Debugger` allows us to interact with the code.

                `import pdb

                def add(num1, num2):
                    pdb.set_trace()
                    return num1 + num2
                    
                add(4, 'hjsdgfuh')`

`pdb` is a way to simulate the execution of your code in the command line. It's a way of testing your code within the command line without actually running the code in the command line.

The computer will pause the code after the line `pdb.set_trace()` and you can view or manipulate it.