---
layout: post
title: Functons & Stuff
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript, coding, learning]
comments: true
---

## Functions are apparently difficult

Functions like:
                `alert("Beware the boogeyman!")`
                `prompt("Enter the name of your fav beer!: )`

Arguments are what you put into functions like these.
                `console.log("Hello!" , "How are you?")`

**console.log** is a function, and what you put inside the () parenthesis is considered an **argument**

## Function Declaration

                `function sayHello() {
                    console.log("Hello!");
                }`
This only declares what the function is and what the arguments are.

Then in order to call said function you can type:
                `sayHello()`

## Anonymous Functions

                `var sayBye = function() {
                    console.log("Bye Bye!");
                }
                sayBye();`

This technically creates a nameless function. And this is apparently a useful method of making functions in certain scenarios.

## Ways to combine multiple arguments and variables

                `function sing(song){
                    console.log(song)
                }
                sing("Crazy!");
                sing("But that's how it goes!");
                sing("Millions of people!");
                sing("Living as foes!");`

Arguments allow us to not have to repeat ourselves. And makes functions more extensible.

                `function multiply(a, b) {
                    console.log(a, b);
                    return a * b;
                }
                multiply(5, 10);

***Return*** is the final way to end a function. The program exits after the final sum is printed to the console or whatever.

**If statements** will not change the outcome of a return function.
