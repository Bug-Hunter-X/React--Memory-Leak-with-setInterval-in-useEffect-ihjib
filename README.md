# React useEffect setInterval Memory Leak

This example demonstrates a common error in React applications: a memory leak caused by improper use of the `setInterval` function within the `useEffect` hook.

The `bug.js` file contains the buggy code. The component uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component unmounts, leading to a memory leak. 

The `bugSolution.js` file provides a corrected version that uses the cleanup function to clear the interval.

## How to reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter incrementing. Then unmount the component and check your browser's developer console for any error or warning.  The original code will not clear the interval causing a memory leak. The solution code will clear the interval correctly.