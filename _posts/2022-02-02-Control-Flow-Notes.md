---
layout: post
title: Control Flow
subtitle:
gh-badge: [star, fork, follow]
tags: [javascript coding learning]
comments: true
---

## Controlling the Flow

This is referring to how JavaScript is a more linear language. But what if there was a way to use conditionals? Such as setting a variable to recognize a username or not?

## If statements

                `var name === "Billy";
                if (name === "Billy"){
                    alert ("Hi Billy";)
                }`

## Else statements

                `var name === "Billy";
                if (name === "Billy"){
                    alert ("Hi Billy";)
                } else {
                    alert ("Hmm, I don't know you");
                }`

This is honestly **no different** from Python if statements. Syntax appears to only be slightly different. Except perhaps that Python might be better for backend stuff.

## Else If (again more like Python)

                `var name === "Billy";
                if (name === "Billy"){
                    alert ("Hi Billy";)
                } else if (name === "Suzy") {
                    alert ("Hi Suzy!");
                } else {
                    alert ("Hmm, I don't know you");
                }`
So if I understand correctly. **If statements** allow you to start a conditional. **Else if** adds what I can only refer to as a stack of conditionals related to the initial one.

Then **else** is the final check if none of the other conditionals are met.

This allows for simple, but complex logic to be added to webpages.
