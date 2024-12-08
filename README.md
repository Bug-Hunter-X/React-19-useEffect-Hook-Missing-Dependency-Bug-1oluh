# React 19 useEffect Hook Missing Dependency
This repository demonstrates a common bug in React 19 related to the `useEffect` hook.  When a value used inside the `useEffect` is not included in its dependency array, it can lead to unexpected re-renders and potentially infinite loops. This example showcases the issue and its solution.

## Bug
The `bug.js` file contains a component with a `useEffect` hook that's missing a dependency.  This causes the component to re-render infinitely because the `count` variable changes inside the effect itself, but it's not listed in the dependencies. 

## Solution
The `bugSolution.js` file demonstrates the corrected code. By including `count` in the dependency array, the `useEffect` only runs when the `count` value changes. This resolves the infinite re-render problem.