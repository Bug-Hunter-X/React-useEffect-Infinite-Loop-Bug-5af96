# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by an incorrect dependency array.  The `useEffect` hook's second argument is an array of values that it uses to track changes. If a value within that array changes between renders, the `useEffect` will re-run.  If the `useEffect` itself modifies a value in the dependency array, it can create an infinite loop.

The `bug.js` file shows the buggy code.  The `bugSolution.js` file provides the correct implementation.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop in the console and the rapidly increasing counter (in the buggy example).