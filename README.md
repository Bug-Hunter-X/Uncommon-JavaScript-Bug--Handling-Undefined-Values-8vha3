# Uncommon JavaScript Bug: Handling Undefined Values

This repository demonstrates a subtle bug in JavaScript related to handling undefined values in a function. The bug occurs when the function receives `undefined` instead of `null` as input, resulting in unexpected behavior.

## Bug Description

The `myFunc` function attempts to handle `null` values correctly by returning 0 if either parameter is `null`. However, it fails to account for situations where a parameter is `undefined` which will result in `NaN`  if a mathematical operation is performed. This is a subtle bug because `undefined` and `null` are often treated similarly but have distinct behaviors. 

## Solution

The solution modifies the function to explicitly check for both `null` and `undefined` values, ensuring that the function behaves consistently regardless of the input type.

## How to Reproduce

1. Clone this repository.
2. Open `bug.js` to see the buggy code.
3. Open `bugSolution.js` to see the fixed code.
4. Run both files in a JavaScript environment (e.g., Node.js) to compare outputs and observe the different behavior.