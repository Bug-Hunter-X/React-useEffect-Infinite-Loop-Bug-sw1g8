# React useEffect Infinite Loop Bug
This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by an incorrectly specified dependency array.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Bug Description
The `useEffect` hook is used to perform side effects after render.  If the dependency array is missing a value that changes within the component, the effect will run continuously, resulting in an infinite loop and potential crashes.

## Solution
The solution involves adding the `count` state variable to the dependency array of the `useEffect` hook. This ensures the effect only runs when `count` changes.