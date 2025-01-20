# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications: an infinite loop caused by an incorrectly used `useEffect` hook.  The `useEffect` hook, when not properly managed, can lead to performance issues and unexpected behavior.

## The Problem

The `bug.js` file contains a `MyComponent` component that utilizes the `useEffect` hook without the correct dependency array.  This causes the effect to run after every render, creating an infinite loop.

## The Solution

The `bugSolution.js` file shows the corrected code.  The key change is including the `count` variable in the dependency array.  By doing so, the effect only runs when the `count` value changes, resolving the infinite loop problem.

This example highlights the importance of carefully considering and specifying the dependencies within the `useEffect` hook's dependency array to avoid common pitfalls.