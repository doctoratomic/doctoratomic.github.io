---
layout: post
title: Scope in JavaScript
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript, coding, learning, advanced]
comments: true
---
### What is Scope?

Scope == variable access. What variables do you have access too when code is run?

By default you are in the `root scope` which is the window object.

Setting variables within a function will only exist in that function.

Lets say I do the following:

                `function aa () {
                    var b = "Hi there!";
                }`

Calling this variable would not be possible without calling this function. As it only exists within this function. Thus, in a way, functions are just more advanced variables. Except they store a larger amount of instructions for a specific purpose within the program.

**A root scope** simply refers to global variables that are directly attributed to the window.

**A child scope** refers to the scope within another function. So these scopes are treated seperately.

Using a similar naming system like Andre does with `var fun = 5;` essentially overwrites a variable just like you would if you did it outside of the function. Meaning the function within JavaScript is essentailly a container for instructions, simplified. Good for referencing a repetitive task that needs to be accessed without rewriting the code over and over again.

Issues that relate to this are called ***Naming Conflicts*** and supposedly you will lose access to the root scope by doing this.

**Functions can access the global variables, but not the reverse.** Meaning that functions can contain their own set of variables and contain them as well as reference variables on the global scope.
