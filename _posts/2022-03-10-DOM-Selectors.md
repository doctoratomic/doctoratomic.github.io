---
layout: post
title: DOM Selectors
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript coding learning]
comments: true
---

## DOM Selectors, and What You Can Do With Them

Since the window of a browser can be read as an object in JavaScript. The document is the object within that contains the raw HTML and CSS data.

Which then with JavaScript, you can access and manipulate the data through these objects. Since the data inside `window` is essentially an array of data.

### Get Elements selector

`document.GetElementsByTagName("h1");` will yield all the data relating to the HTML file that has this tag. Likely every single one of them if there are multiple.

`document.GetElementsByClassName("class");`

`document.GetElementsById("idname");`

All of these allow you to extract the specified data from an HTML source.

### Query Selector

`document.querySelector("h1");` This will give you access to the first bit of data the selector finds. So if you're extracting from a `<ul>` element, it will only select the first on the list.

`document.querySelectorAll("li");` however, will select all of the variables in the list. Adding other elements like `<h1>` will change the heirarchy of the data. Presenting the `h1` element before the `li` in an array on the console.

Thankfully, this feature is supported on [CanIUse.com](https://caniuse.com/?search=queryselector)!

### Get & Set Attribute Selector

To use this function, you have to declare what exactly is the element you are selecting.

So going `document.querySelector("li");` and then either storing the data in a variable or use `document.querySelector("li").getAttribute("random");`. `random` is of course the name of the attribute used in the video for the Udemy course I am following. But this can simply be the name of the element, class, or id. Thus specifying your search for whichever elements data you need.

`document.querySelector("li").setAttribute("random", "1000");` will then change the value from `23`. Though it will return `undefined` in the console on Chrome.

### Changing Styles

Using a function `.style` on the tail end of the Query selector will then allow you to adjust the CSS style on command.

`document.querySelector("h1"),style.background = "green";` will then change the background of the text into green.

This is actually really interesting to finally figure this out. As I've wondered what exactly these functions mean. Another one of Andre's classes involve doing projects exclusively. And thus using some of these functions to make cool websites.

However, this function adds the element directly to the HTML. Instead we should focus on adjusting the CSS file instead.

To do that, you can add the call for the `h1` element to a variable like this:

`var h1 = document.querySelector("h1");`

Then go: `h1.className = "coolTitle";`

This points this heading directly to the class you choose on the CSS file. And you can even find cool title designs for CSS code for [free!](https://codepen.io/)

### Class List

This function allows you to add and remove classes from within a list of data.

`document.querySelector("li").classList;` will print a blank array if there are no classes added to the element called. However, it will display a list of every class within the element otherwise.

`document.querySelector("li").classList.add("coolTitle");` will then add a class within the CSS and assign it to the html element.

`classList.remove` will then remove the class from a selected element.

`classList.toggle` will essentially act as a boolean to an element. Andre uses a linethrough element in his shopping list to indicate when something is done or not. Effectively turning a style on or off again.

However, looks like [less and less browsers](https://caniuse.com/?search=classList) are capable of supporting this function.

### Inner HTML

`.innerHTML` is a function that will easily edit inside of another element.

`document.querySelector("h1").innerHTML = "<strong> HELLLO !!! </strong>";` This will then replace anything within that element, in favor of what was added in it's place.

### Parent Elements & Children

`document.querySelectorAll("li")[1].parentElement;` This retrieves the parent of the element selected. In this case, it would be for the `<ul>` that encompasses this `li` element. Stacking on `.parentElement.parentElement` only goes further up the ladder in HTML heirarchy.

Adding `.children` after `.parentElement` will then print all of the elements to the HTML element that stem from that single element selected. In the case of the `body` or the `ul` it would be the contents of the body.

`It's important to CACHE selectors in variables`
