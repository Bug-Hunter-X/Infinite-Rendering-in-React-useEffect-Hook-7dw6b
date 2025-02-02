# Infinite Rendering in React useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook, leading to infinite rendering. The error stems from the missing dependency array, causing the effect to run on every render, creating an infinite loop.

## Bug Description
The `useEffect` hook in `MyComponent` has no dependency array ([]). This leads to it running on every render, triggering a new render, and the cycle continues.

## Solution
The solution is to include the `count` variable in the dependency array. This ensures the effect only runs when `count` changes.