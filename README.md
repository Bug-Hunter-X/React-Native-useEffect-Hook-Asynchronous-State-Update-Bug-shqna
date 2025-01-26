# React Native useEffect Hook Asynchronous State Update Bug

This repository demonstrates a common bug in React Native applications involving the `useEffect` hook and asynchronous state updates. The bug arises when attempting to update state within the `useEffect` callback, leading to unexpected behavior or even infinite loops because the component may re-render before the state change has fully taken effect.

## Problem
The provided `bug.js` file contains a React Native component that tries to increment a counter using `setCount(count + 1)` within the `useEffect` hook.  Since state updates in React are asynchronous, `count` in the callback refers to the previous state value, causing the counter to increment incorrectly or infinitely.

## Solution
The `bugSolution.js` file provides the corrected implementation. It uses a functional approach to update the state, ensuring the latest state value is used.