# Unnecessary Re-renders in React's useEffect Hook

This repository demonstrates a common React bug: an `useEffect` hook that runs after every render, leading to unnecessary computations and potential performance problems.

## Bug Description
The `useEffect` hook in `bug.js` logs the current count to the console after each render.  This is inefficient, especially if the component updates frequently.  This behavior makes the app inefficient and impacts performance in larger scale apps.

## Solution
The `bugSolution.js` file shows the correct implementation. Using the optional dependency array `[]` ensures that the useEffect only runs once after the initial component render, eliminating extra console logs.