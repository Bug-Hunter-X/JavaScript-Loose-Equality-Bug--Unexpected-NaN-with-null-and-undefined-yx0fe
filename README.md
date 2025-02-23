# JavaScript Loose Equality Bug

This repository demonstrates a common JavaScript bug related to loose equality (==) when handling null and undefined values. The bug arises from JavaScript's type coercion during comparisons.

## Problem Description

The provided `foo` function intends to handle `null` values by returning 0. However, when `undefined` is passed, it unexpectedly returns `NaN`. This occurs because `null == undefined` evaluates to `true` due to loose equality, causing the `else` block to execute with the addition of `undefined + 1`. Since you cannot add 1 to undefined, the result becomes `NaN`.

## Solution

The solution involves using strict equality (===) to ensure that only `null` is handled specifically.  This avoids implicit type conversion and leads to more predictable and reliable behavior.

## How to Run

1. Clone this repository.
2. Open `bug.js` to see the buggy code.
3. Open `bugSolution.js` to see the corrected code.
4. Run the JavaScript code using a Node.js runtime or any JavaScript environment (e.g., browser console).
