# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common issue encountered when using closures within `setTimeout` loops in JavaScript.  The problem arises because the loop's counter variable `i` is not captured correctly within each callback function.

The `bug.js` file contains the erroneous code.  The `bugSolution.js` file provides the corrected solution.

## Problem

The expected behavior is to log the numbers 0 through 9 with a one-second delay between each number. However, due to the closure issue, all callbacks will log the final value of `i` (which is 10) after the loop completes.

## Solution

The solution involves using an immediately invoked function expression (IIFE) to create a new scope for the variable `i` within each iteration of the loop, ensuring that the correct value is captured.