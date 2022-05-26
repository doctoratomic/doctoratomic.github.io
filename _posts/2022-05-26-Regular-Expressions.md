---
layout: post
title: Regular Expressions
subtitle: with Python!
gh-badge: [star, fork, follow]
tags: [python, coding, learning, regular expressions]
comments: true
---

### What are they?

Not unique to Python

Useful for finding things in a piece of text.

`import re` imports the library.

This module is similar in function to `Perl`

                `import re
                
                pattern = re.compile(r"(^[a-zA-Z0-9]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$)")
                string = "Matthew"
                a = pattern.search(string)
                print(a)`

Essentially these expressions are indicated through an entirely new syntax.

One that can be easily made using some [tools.](https://regex101.com/)