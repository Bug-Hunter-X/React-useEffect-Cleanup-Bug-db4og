# React useEffect Cleanup Bug

This repository demonstrates a common bug in React's `useEffect` hook: forgetting to return a cleanup function. This can lead to memory leaks and unexpected behavior, especially when dealing with asynchronous operations or subscriptions.

## Bug
The `bug.js` file contains a component that logs a message when it mounts, but it does not include a cleanup function in the `useEffect` hook. This means that the log message is called only once, on mount, but it never stops.  This is not an error, but if the component is frequently mounted and unmounted, this behavior could cause issues.   To correct this, the effect should be properly cleaned up.

## Solution
The `bugSolution.js` file shows the corrected code. It includes a cleanup function which will log the correct message upon unmount. 
