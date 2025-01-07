# React useEffect Runs After Every Render

This repository demonstrates a common issue in React applications where the `useEffect` hook runs after every render, leading to performance problems and potentially unexpected behavior. The problem is often caused by missing dependencies in the dependency array or including unnecessary dependencies.

## Bug

The provided `MyComponent` uses `useEffect` without specifying a dependency array or with an incomplete one.  This means the effect will run on every render, potentially causing unnecessary re-renders or unexpected side effects.  In this specific example, the console log will repeatedly print updated count, even for non-relevant state changes.

## Solution

The solution involves correctly specifying the dependencies in the useEffect's dependency array. If the effect only needs to run when a specific state variable changes, include only that state variable in the array.