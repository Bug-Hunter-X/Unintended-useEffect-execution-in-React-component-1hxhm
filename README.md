# Unintended useEffect Execution in React

This repository demonstrates a common React bug involving the `useEffect` hook. The `useEffect` hook, without an empty dependency array (`[]`), re-renders after every state change, leading to performance issues and potentially unexpected behavior.

## Bug Description

The provided `MyComponent` uses `useEffect` to log the current count.  Without a dependency array, the effect runs after every render, including the initial render and after each click of the button. This is inefficient and may lead to unexpected behavior, especially with more complex side effects.

## Solution

The solution involves providing an empty dependency array (`[]`) to `useEffect`. This ensures the effect only runs once after the initial render, avoiding unnecessary re-renders.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the application's behavior.
