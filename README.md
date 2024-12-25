# JavaScript Closure Gotcha in setTimeout Loop

This repository demonstrates a common issue in JavaScript related to closures and the `setTimeout` function within loops. The problem arises when trying to use the loop variable inside a callback function of `setTimeout`.

## The Bug

The provided `bug.js` file contains a function `myFunc` that uses a `for` loop and `setTimeout`. It intends to log numbers 0 through 9 with a one-second delay. However, due to the way closures work in JavaScript, it logs `10` ten times.

## The Solution

The solution provided in `bugSolution.js` demonstrates how to fix this using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop. This ensures that each iteration's value of `i` is captured correctly. 

## How to run the code

Simply save the `bug.js` and `bugSolution.js` files and then run them using Node.js:

```bash
node bug.js
node bugSolution.js
```