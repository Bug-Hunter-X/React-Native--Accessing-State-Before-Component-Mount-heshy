# React Native: Accessing State Before Component Mount

This repository demonstrates a common issue in React Native: attempting to access component state before it has been fully mounted. This often leads to unexpected behavior or crashes.  The solution involves carefully considering the lifecycle of the component and using appropriate methods to ensure state is available before access.

## Bug Report

The `bug.js` file shows an example where an `useEffect` hook attempts to access a state variable before it has been initialized. This results in undefined values being used in the component.

## Solution

The `bugSolution.js` file shows a solution using a conditional check to only access the state variable after it has been initialized.  Alternatively, you can move the code that depends on the state into another effect that runs after the state is set. 