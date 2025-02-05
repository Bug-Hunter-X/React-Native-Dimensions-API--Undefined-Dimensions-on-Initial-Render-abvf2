# React Native Dimensions API: Undefined Dimensions on Initial Render

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native. The problem arises because the dimensions are not always immediately available, particularly on app startup or when the screen orientation changes.

## Bug Description

Accessing `Dimensions.get('window')` before the dimensions are fully loaded results in undefined values for `width` and `height`, potentially leading to app crashes or unexpected behavior.  The `bug.js` file shows the problematic code.

## Solution

The solution involves using the `Dimensions` API's `addEventListener` to listen for changes in screen dimensions and update the component's state accordingly.  This ensures the component always has access to the correct values. The solution is implemented in `bugSolution.js`.