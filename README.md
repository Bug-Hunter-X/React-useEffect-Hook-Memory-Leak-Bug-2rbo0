# React useEffect Hook Memory Leak Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook: missing a return statement for cleanup functions.

## Bug Description
The `useEffect` hook in the `MyComponent` component lacks a return statement for cleanup.  This can lead to memory leaks if the component unmounts before the cleanup function has executed.  In this example, the `console.log` statement is harmless, but it illustrates the principle.

## Bug Solution
The solution involves adding a return statement to the `useEffect` hook, which provides a function to run when the component unmounts or when dependencies change.  This ensures that any cleanup actions (like timers, event listeners, or subscriptions) are properly handled, preventing potential leaks.