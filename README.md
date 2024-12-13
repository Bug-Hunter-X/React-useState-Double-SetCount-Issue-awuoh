# React useState Double SetCount Issue

This repository demonstrates a common issue in React when using the `useState` hook and calling `setCount` multiple times in quick succession.  Due to React's batching of updates, the count may not increment by the expected amount.

## Bug Description
The `bug.js` file contains a React component that increments a counter.  However, calling `setCount` twice in the `handleClick` function does not result in the counter incrementing by two; it only increments by one because of React's update batching system.

## Solution
The `bugSolution.js` file demonstrates a solution using the functional update pattern of `setCount`.  By passing a function to `setCount`, the update is calculated based on the latest state value, ensuring the counter increments by two.