# React Memory Leak Bug
This repository demonstrates a common React bug: memory leaks caused by improper cleanup in useEffect hooks using setInterval.  The bug.js file shows the flawed component, while bugSolution.js provides the corrected version.

## Bug Description
The `MyComponent` component uses `setInterval` to update a counter every second. However, it lacks a cleanup function within the `useEffect` hook.  This means that when the component unmounts, the `setInterval` continues to run, leading to a memory leak.  This is a very common problem for developers new to React's lifecycle methods.