---
layout: post
title: Intro to Javascript
subtitle: Basic syntax and understanding
gh-badge: [star, fork, follow]
tags: [javascript coding learning]
comments: true
---


## I want to start by first making the assumption that you understand all of the prerequisites to web dev. Including HTML & CSS syntax

Created in 1995 as a way to create actions on websites by Netscape.

The verb of any website (Tweet, Goole it, etc)

Netscape beat the competition because of their early adoption of JS. And this led to the market reacting to this until a standard was set. So everyone was on the same page.

It is a great language for the front and back end of a website!

Go to

> View > Developer > JavaScript Console

And click the Console tab.

This will allow you to experiment with JavaScript within Google Chrome.

JS can do basic mafs.

IE

                `3+4
                7`

I am already familiar with Python and how you can interact with the console.

This is virtually similar in nature. If not exactly the same.

## Strings

                `"Hugh Mungus"`

Using the quotations in JS, you get what is known as a **string**

                `"Hugh" + " Mungus"`

This of course combines the two together. Leaving a space before or after one of them acts as proper grammar.

To us a (') within s string, it will deliver an error.

Instead, do this:

                `"This isn\'t very nice"`

This will return the proper sentence.

                `10 + "34"
                1034`

^^ This also seems similar to Python. Though I do not remember.

However:

                `10 - "3"
                7`

This is because you can't exactly subtract strings from one another.

                `"hello" - "bye"
                NaN = Not a Number`

## Booleans

A statement that is either true or false:

                `3 > 2
                true`

                `5 > 10
                false`

                `3 == 3 will bring a sytnax error
                **Correction** = 3 === 3`


                `!== means **does not equal**`

## Variables

                `var george = "These pretzels are making me thirsty" + "!";`

Rules

- Needs to start with a letter
- Can end with a number
- Can't ***start*** with a number
- Can't start with a symbol
- Can also start with a '$' and an '_'
- "CamelCase" === variableName

                ` prompt()`

Recieves user input to the console.

                `var first = prompt ("enter first number");
                var second = prompt("enter second number");
                var sum =  Number (first) + Number(second);
                alert (sum);`

***var*** sets the variable to a name. Can be a string or number. Or a boolean!

Thus naming the final var as sum and using a basic equation to determine the input amount is how this simple program works.

Using variables in an algorithm to solve a problem. ***Perhaps the essence of programming in general?***

To add to the final code, you could then go:

                 `alert("The sum is: " + sum);`

This final line would then print an alert prompt through the browser to the user.

Also using a semicolon(;) is how you end expressions. As is with many programming languages.

## Undefined

Used when nothing is assigned to a variable.

## Conditionals

### If statements

                `if (name === 'Billy') {
                    alert("Hi Billy!')
                    }`

### Else

                `if (name === "Billy"){
                    alert("hi Billy");
                    } else {
                    alert("hmmm I don't know you...");
                    }`

### Else If

                `if (name === "Billy"){
                    alert("Hi Billy");
                    } else if (name === "Suzy") {
                        alert("hi Suzy!");
                    } else {
                        alert("I don't know you");
                    }`

These kind of conditionals allow you to add all kinds of specific circumstances depending on input!

At least, I like to hope it's that simple...

## Logical Operators

                `if (name === "Billy || name === "Ann") {
                    alert("Hi Billy or Ann");
                }`

This allows you to use the "||" brackets to essentially set multiple variables in an either or kind of situation. Thus setting multiple variables in one.

IE. I can use one ***if statement*** to add multiple variables to it.

You can use **&&** to essentially combine two different variables in an if statement.

                `firstName = "Billy"
                lastName = "Bob"
                if (firstName === "Billy && lastName === "Bob") {
                    alert("Watch out we got a Redneck over here!")
                }`

This allows you to set specific parameters for certain **if statements**.

Meanwhile an (**!**) at the beginning will reverse a boolean.

Meaning, if you type:
                `if(!(firstName === "Billy)) {
                alert("Good to know you're not a redneck lol")
                }`
The alert would only show up if the variable was NOT set to "Billy". Some would say that this function acts like a ***light switch***, and turns the variable off and on again.
