---
layout: post
title: DOM Events
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript coding learning]
comments: true
---
## DOM Events

So this is how most active elements are programmed onto the page. Such as when you move a mouse towards a corner, or away from the page. A pop up will appear to grab the attention of the user.

[Here is a detailed list referencing all of the types of events JavaScript can listen for.](https://developer.mozilla.org/en-US/docs/Web/Events)

[Here also, is a list of character codes for keyboard inputs.](https://www.cambiaresearch.com/articles/15/javascript-char-codes-key-codes)

VSCode and Sublime find problems in the syntax that Andre types out on video.

But he goes over how best to refactor code. Which is essentially breaking down his functions even further into steps. Naming variables that he then calls later to use for his overall program.

This is nice to see how it works, as I will begin working on a project that can outline a screenplay down to the very beats of a scene. It'll be a form with an editable hierarchy that can be added to or removed from.

Acts > Sequences > Scenes > Beats

You'll be semi limited by what you can add at first. Maybe a pro feature to make it unlimited?

### A Note About Callback Functions

In the previous video you saw something interesting:

Event listener syntax :

                `button.addEventListener("click", addListAfterClick);
                input.addEventListener("keypress", addListAfterKeypress);`

You didn't see the function being called like this as you may have expected:

                `button.addEventListener("click", addListAfterClick());
                input.addEventListener("keypress", addListAfterKeypress(event));`

This is something called a callback function. When that line of javascript runs, we don't want the `addListAfterClick` function to run because we are just adding the event listener now to wait for click or keypress. We want to let it know though that we want this action to happen when a click happens. So the function now automatically gets run (gets added the `()`) every time the click happens. So we are passing a reference to the function without running it.
