# Unhandled Promise Rejection in Express.js Async Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections within asynchronous request handlers.  The application does not gracefully handle errors, leading to crashes.  The solution showcases proper error handling using `.catch()` and centralized error handling middleware.

## Bug

The `bug.js` file contains an Express.js application with an asynchronous route handler (`/`) that may throw an error.  The application lacks proper error handling, causing it to crash silently if the asynchronous operation fails.

## Solution

The `bugSolution.js` file provides a solution by adding a `.catch()` block to the promise chain within the route handler, and implementing a global error-handling middleware.