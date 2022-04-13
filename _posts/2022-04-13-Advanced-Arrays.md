---
layout: post
title: Advanced Arrays
subtitle: JavaScript
gh-badge: [star, fork, follow]
tags: [javascript, coding, learning, advanced]
comments: true
---

`var array = [1,2,10,14];`

`const double = []
const newArray = array.forEach((num) => {
    double.push(num * 2);
})`

### Map, Filter, Reduce

#### Map

`const mapArray = array.map((num) => {
    return num * 2;
})

console.log(mapArray);`

`Map` is good for use with simple loops in arrays over `forEach`. The operation with `forEach` might do nothing. All it cares about is to iterate over a collection of elements. And then apply the operation on each element.

`Map` has a restriction to the operation. It creates its own array, and returns the results within that new array. To do that with `forEach` you would need to create an empty array to dump the data into?

With `Map` it just automatically sets parameters for itself to make the process of adjusting these values easier.

A cleaner version of the above code would look like this:

                `const mapArray = array.map(num => num * 2);`

Great principles to have when refactoring code.

#### Filter

`const filterArray = array.filter(num => {
    return num > 5
})`

This function filters out data within an array based on the parameters of the script. In this case, it ignores anything less than 5, and creates a new array with the two remaining numbers that are greater than 5.

You can apply these to strings, integers, and booleans too probably. Either way, like `map` it also creates a new array from the data.

#### Reduce

`const reduceArray = array.reduce((accumulator, num) => {
    return accumulator + num
}, 0);

console.log(reduceArray);`

Accumulator stores information that happens in the body of the function. You set the value at the end of the return function. In this case it is set to `0` and then reduces all the numbers to their combined sum.
