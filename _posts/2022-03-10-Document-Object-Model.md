---
layout: post
title: Document Object Models
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript coding learning]
comments: true
---

### DOM = Document Object Model

JavaScript essentially allows actions to performed on CSS and HTML pages.

Which allows for things like Chrome Extensions being able to adjust webpages in real time. Since web pages are simply requested from their server and copied to your computer.

                `document.write("Hello!")`

This enables you to change the document you've copied, using a built in function of JavaScript.

Each browser has a JavaScript engine:

***Chrome*** = V8 Engine
***Edge*** = ChakraCore
***Safari*** = Nitro
***FireFox*** = SpiderMonkey

They read the JavaScript file line by line and execute the code.

Web browsers allow us to access the **DOM (Document Object Model)** which we can then adjust or modify with JavaScript on our end.

The parent object is called "window". It describes the browser and it's structure that your using.

                `window.alert("check check");`

You cannot write to this object. Only to the contents of said object. Such as using a scraping plugin to search for data within the window to extract?

This essentially explains to me why JavaScript is not only very widely used. But frankly a powerhouse of a tool. This must be how most Google Chrome plugins work. By adding a script to activate when certain conditions are met, the HTML can then be modified in real time. Changing or accessing anything within the DOM's window.

It's very clear that this is how JavaScript is being used today. And in concert with other backend languages like Python and SQL.

All of this is the key to building cool tools for the internet.
