# Infinite Loop in useEffect Hook with Count Dependency

This repository demonstrates a common error in React applications involving the `useEffect` hook.  Improper use of dependencies in `useEffect` can easily lead to infinite render loops, significantly impacting performance.

## The Bug

The `bug.js` file contains a component with a `useEffect` hook that depends on the `count` state variable.  Because the `setCount` function updates the `count` state, which then triggers a re-render and another execution of the `useEffect` hook, an infinite loop results.

## The Solution

The `bugSolution.js` file provides a corrected version. The unnecessary re-render is avoided by carefully managing dependencies in the `useEffect` hook.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs. You'll notice that the original code logs repeatedly and causes React to slow down. The solution will fix the problem.