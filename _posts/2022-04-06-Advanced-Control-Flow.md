---
layout: post
title: Advanced Control Flow
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript coding learning advanced]
comments: true
---
### The Ternary Operator

**condition ? expr1 : expr2;**

Essentially an easier method to use booleans in conditionals.

For example:

                `function isUserValid(bool) {
                    return bool;
                }
                
                var answer = isUserValid(true) ? "You may enter" : "Access Denied";`

This appears to just be a simpler method to building if and else statements easier.

Perfect for checking a condition with only two possible outcomes.

### Switch Statements

                `function moveCommand(direction) {
                    var whatHappens;
                    switch (direction) {
                        case "forward":
                            whatHappens = "You encounter a Headhunter";
                            break;
                        case "back":
                            whatHappens = "There is no going back now...";
                            break;
                        case "right":
                            whatHappens = "You enter a bar full of shady characters";
                            break;
                        case "left":
                            whatHappens = "You hear the scream of a chimera off in the distant forest.";
                            break;
                        default:
                            whatHappens = "You must go SOMEWHERE!";  
                    }
                    return whatHappens;
                }`

**Switch statements are a great alternatives to Else If Statements.** The code cycles through and checks all of these options to see whether any of the conditions were met and acts accordingly. Otherwise it moves to the default response. Pretty good for RPG style adventures it seems!

`break;` skips over the other statements in the code and goes straight to the final `return whatHappens;`