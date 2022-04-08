---
layout: post
title: Advanced Functions
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascrip coding learning advanced]
comments: true
---

## Const Is Just Another Means to Write Functions

                `const first = () => {
                    const greet = 'Hi';
                    const second = () => {
                        alert(greet);
                    }
                    return second;
                }`

### Closures

A function ran. The function executed. It's never going to execute again. BUT it's going to remember that there are references to those variables. So the child scope always has access to the parent scope.

Children always have access to their parent scope. But parents do not have access to their children.

### Currying

The proccess of converting a function that takes multiple arguments into a function that takes them one at a time.

                `const multiply = (a, b) => a * b;
                const curriedMultiply = (a) => (b) => a * b;
                curriedMultiply(3);`

Using the `=>` essentially acts as a function?

Thus anything that comes after it serves as a function.

Thus calling the above script like so: `curriedMultiply(3)(4);` returns the answer of the integers provided.

You can use this to create constant functions that serve a specific purpose.

                `const multiplyBy5 = curriedMultiply(5);
                multiplyBy5(5);`

Now you can call this function at any point whenever you want to multiply by 5.

### Compose

The act of putting two functions together, to form a third function where the output of one function is the input of the other.

                `const compose = (f, g) => (a) => f(g(a));
                
                const sum = (num) => num + 1;
                
                compose(sum, sum)(5);`

I guess this is where basic PEMDAS comes in handy. As this function calculates the sum based on the postitions the function has within the parentheses. `5` is the `a` in this function. `g` then becomes `sum` which equals the sum plus one. Thus making it `6`.

`const compose = (f, g) => (a) => f(6)`

Then finally the `f` function runs. Which is also sum. Adding another plus one to the final answer. Which becomes `7`.

### Avoiding Side Effects & Functional Purity

Essentially Andre is saying that you should avoid contradictory code within your functions. Such as having functions affect variables within the global scope. Rather than within the function. And it can negatively affect the code and cause bugs.

Functional purity is when this doesn't happen, and the code always outputs the correct consistent output every time.

By avoiding side effects, and always returning is called **Deterministic** which means consistency within the code that results in output regardless of the input of the code.
