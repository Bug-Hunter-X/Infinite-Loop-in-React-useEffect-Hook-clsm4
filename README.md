# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to a missing dependency in the effect's dependency array.

## The Bug

The `bug.js` file contains a React component that uses `useEffect` to log the current count.  However, because the `count` variable isn't included in the dependency array, the effect runs after every render, leading to an infinite loop and console spam.  This is a classic mistake easily made when not paying close attention to the dependencies needed for your effect.

## The Solution

The `bugSolution.js` file shows the corrected code.  By including `count` in the dependency array `[count]`, the effect only runs when the `count` value changes, preventing the infinite loop.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the infinite loop in the console for `bug.js` and correct behavior in `bugSolution.js`.
