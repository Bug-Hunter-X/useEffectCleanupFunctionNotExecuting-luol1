# React useEffect Cleanup Function Issue

This repository demonstrates a problem with the cleanup function in React's `useEffect` hook. The cleanup function is not consistently executing as expected. 

## Problem Description
The issue occurs when the component renders and unmounts, the cleanup function within the `useEffect` hook is supposed to log a message to the console.  However, in some instances, the message is not logged. This inconsistency leads to unpredictable behavior and potential memory leaks if resources are not properly released.

## Solution
The solution involves carefully inspecting the dependency array and ensuring that the effect is correctly managed.  In the provided solution, the unnecessary dependency `count` was removed from the dependency array, ensuring the effect only runs once, on mount. This prevents the cleanup from running too frequently.