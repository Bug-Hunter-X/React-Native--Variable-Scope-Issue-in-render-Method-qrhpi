# React Native Variable Scope Issue in render Method

This repository demonstrates a common error in React Native: incorrectly using variables declared inside a component's render method.  The `bug.js` file shows the problematic code, where a counter variable is declared within the render method.  This variable is re-created on every render, leading to an unexpected behavior. The `bugSolution.js` file provides the correct solution.

## Problem

In React Native, values declared within the `render()` method do not persist across renders.  Attempting to update such variables directly will not correctly reflect the changes in the UI.

## Solution

To correctly manage state that should persist across renders, use the `useState` hook or the `this.state` object (for class components).  This allows React to track changes efficiently and update the UI accordingly.

## How to run

1. Clone the repository
2. Navigate to the project directory
3. Run `npm install`
4. Run `npx react-native run-android` or `npx react-native run-ios`