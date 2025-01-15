# Unexpected NaN Comparison in JavaScript

This repository demonstrates a common, yet subtle, error in JavaScript related to comparing NaN (Not a Number) values.

## The Bug
The issue stems from the fact that `NaN` is not equal to itself, regardless of whether you use strict (`===`) or loose (`==`) equality comparison.

The `bug.js` file contains a simple function that attempts to compare two numbers for equality.  However, if both numbers are `NaN`, the function incorrectly returns `false`.

## The Solution
The `bugSolution.js` file provides a corrected version of the function.  Instead of directly comparing using `===` or `==`, we use the `Number.isNaN()` function to explicitly check for `NaN` values.

This approach correctly identifies `NaN` and handles the comparison accordingly.