# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook causing an infinite render loop.  The bug arises from omitting the dependency array in `useEffect`, leading to the effect running after every render.

## Bug Description
The `MyComponent` uses `useEffect` to log the current count to the console after each render.  Since the `count` state changes with every click, the `useEffect` function is called repeatedly, creating an infinite loop and flooding the console.

## Solution
The solution involves correctly specifying a dependency array in `useEffect`. This array should list all state variables and props that the effect relies on. If no dependencies are needed, specify an empty array `[]`.