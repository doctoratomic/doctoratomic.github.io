---
layout: post
title: What Are Arrays?
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript, coding, learning]
comments: true
---

## Data structures allow us to store information in formats that can be useful to developers

If variables are like desk drawers, arrays are the means in which to organize them. Like folders in a desk!

            `var listOfPlanets = ["naboo", "tatooine", "dagobah", "hoth", "mustafar"];
            console.log list[1];`

The above array would print "tatooine" on the console. Because computers start counting at 0 and then 1. Making tatooine the planet of our choice.

Arrays can store numbers, booleans, strings, variables, and functions! You can even add multiple different types of data in an array!

Though it is more efficient to put the same type of data within its own array.

You can also save arrays within arrays!

                `var list = [
                    ["naboo", "tatooine", "dagobah", "hoth", "mustafar"]
                ];
                console.log list[1][1];`

## Arrays, How Do They Work?

                `var list = [
                ["naboo", "tatooine", "dagobah", "hoth", "mustafar"]
                ];
                console.log list[1][1];


                list.shift(); /* Moves list to the left. Removing zero */

                list.pop(); /* Removes last number in array in this case "mustafar" */

                list.push("dantooine"); /* This ads to the array */

                list.sort(); /* Alphabetizes contents of list */

                list.concat(["yavin IV","coruscant","kashyyyk"]);

                var newList = list.concat(["yavin IV","coruscant","kashyyyk"]);

                /*
                Using list.concat will only add to the list temporarily. When you try to sort this data, it will only print the defined list.
                What you must do instead, is make a new variable that makes that concat merge with the others. 
                */`
