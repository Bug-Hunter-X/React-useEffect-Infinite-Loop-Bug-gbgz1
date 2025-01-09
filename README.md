# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## The Bug

The `bug.js` file contains a `MyComponent` that uses the `useEffect` hook to log the current value of a `count` state variable. However, the `count` variable is not included in the dependency array of the `useEffect` hook which causes an infinite loop.  The component re-renders, updating the `count` state, causing the effect to run again, and so on.

## The Solution

The `bugSolution.js` file corrects this by including `count` in the dependency array. Now, the effect only runs when the `count` variable changes.