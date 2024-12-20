# React useEffect Dependency Array Issue

This repository demonstrates a common error in React's `useEffect` hook: incorrectly specifying the dependency array.  Improperly defined dependency arrays can lead to unexpected behavior, including infinite render loops or stale closures.

## Bug Description
The `bug.js` file contains a `MyComponent` that uses the `useEffect` hook to log the current count to the console. However, the initial implementation omits `count` from the dependency array, resulting in the effect running only once after the initial mount, regardless of changes to the `count` state. This is not the intended behavior. 

## Solution
The `bugSolution.js` file provides the correct implementation, where `count` is included in the dependency array. This ensures that the effect runs whenever `count` changes, providing the desired behavior.

## How to reproduce
1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `npm install` to install the required packages.
4. Run `npm start` to start the development server.
5. Observe the console output and the component's behavior in both files to see the difference.