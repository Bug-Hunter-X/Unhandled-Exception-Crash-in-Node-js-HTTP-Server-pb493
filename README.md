# Node.js Unhandled Exception Bug

This repository demonstrates a common yet easily overlooked error in Node.js: unhandled exceptions within asynchronous operations leading to server crashes.  The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a robust solution.

## Bug Description

The server in `bug.js` lacks proper error handling.  If an unexpected exception occurs during request processing, the server will crash without any graceful error handling.

## Solution

The `bugSolution.js` file demonstrates a solution using `try...catch` blocks to handle exceptions and prevent unexpected crashes.  This allows for graceful error handling and prevents server downtime.

## How to reproduce

1. Clone this repository.
2. Run `bug.js` using `node bug.js`.
3. Observe that the server starts and runs.
4. Try introducing an error in requestListener (e.g., accessing a non-existent property)  to see the crash.