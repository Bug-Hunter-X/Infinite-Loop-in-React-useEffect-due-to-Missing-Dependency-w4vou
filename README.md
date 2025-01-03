# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The issue arises from an incomplete dependency array, leading to an infinite loop.

## Problem

The `MyComponent` component uses `useEffect` to log the current count to the console after every render. However, the dependency array is missing `count`, resulting in the effect running after every render, even if `count` hasn't changed. This creates an infinite loop, filling the console with messages and potentially freezing the browser.

## Solution

To resolve the problem, add `count` to the dependency array. This ensures the effect runs only when `count` changes.

## How to run

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install the required packages.
4. Run `npm start` to start the development server.