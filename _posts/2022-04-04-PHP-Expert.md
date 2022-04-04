---
layout: post
title: Overnight PHP Expert
subtitle: PHP
gh-badge: [star, fork, follow]
tags: [php coding learning]
comments: true
---

## I decided I was going to tackle PHP briefly so I could dive into the Laravel framework

1. Install WAMP/MAMP
2. PHP files
3. Outputting Strings
4. Variables
5. Concatenation
6. Operators
7. If statements
8. Handling data from html forms
9. Arrays
10. Loops

### WAMP and MAMP

[MAMP is for Macs](https://www.mamp.info/en/mamp/mac/)
[WAMP is for Windows](https://www.mamp.info/en/mamp/windows/)

Install these for your subsequent PHP projects.

This will create a folder for the local web server you are working on. And will install likely within the Applications data of your preferred OS.

Some light automation can take you to the home page. Or you could go to localhost:8888/nameofrootfolder

### PHP Within HTML

You can start by creating what is a normal HTML file and rename it to `index.php`.

To start writing the syntax within the HTML by writing `<?php` and ending with `?>`.

Like this:

                `<?php
                    echo "Hello, World!";
                    ?>`

PHP is a language that is executed on the server vs the client. Therefore the user cannot see the PHP from their end.

`echo` is equivalent to `document.write` in JavaScript or `print` in Python. As it outputs the result of the subsequent code.

### Variables

Variables within PHP start with a `$` and often will look like:

                `$myvariable = 17;`

### Concatenation

The process in which you combine strings together. In PHP it would look something like this:

                `$name = "Matt"
                echo "Hello " . $name;`

Then the output becomes "Hello Matt" when executed.

### Operators

Operators in PHP seem to be similar to operators in JavaScript as well.

`+` addition

`-` subtraction

`*` multiplication

`%` division

**Comparison Operators:**

== means equal to ($x == $y) this will print a boolean of either true or false.
!== means NOT equal to
**Logical Operators:**
***and*** will return a boolean if both are true
***or*** will return if x or y is true. Or if both are true.

**If statements:**
                `$loggedIn = true;
                if (loggedIn == true) {
                    echo "You are logged in";
                } else {
                    echo "Please log in";
                }`
Pretty standard If statements, similar to JS and Python.

### HTML Forms

In your HTML code you can add the following:
                `<form action="process.php" method="post">
                    Enter your name:<input name="name" type="text">
                    <input type="submit">`

The PHP file can then be called from the HTML file to perform the process after recieving data from the form.

Then in the PHP file you can accept the data from there.

                `<?php
                    $name = $_POST["name"];
                    echo "Hello there " . $name;
                ?>`
Where you put `name` is whatever the name of the name of the tag you added to the html you set.

### Arrays

                `$people = array("Batman", "Superman", "The Flash");
                print_r($people)`

`print_r` will then display the whole array. Numbers and all. To output a single element within an array, simply write `echo $people[2]` which would output "The Flash. As computers always start counting from 0.

### Loops

                `foreach($people as $person){
                    echo $person . ' ';
                }`
This loops through an array. For each element in the `$people` array execute the code and keep going. Stopping only when `$person` is equal to an element in the array.

The code above loops through the data. And prints them all to the HTML file.

Another example:

                `$numbers = array(5,14,201);
                $sum = 0;
                foreach ($numbers as $number){
                    $sum = $sum + $number;
                }
                echo $sum;`

This then adds the total of the numbers together to give us the sum of all three.

Anyway, just some really quick basics into PHP. I want to learn to use Laravel eventually, and since I understand the concepts behind arrays, loops, integers, variables, etc. For me, it is now about how each of them work in each language, and what each language excells at doing.
