# Node.js Server Port Already in Use

This repository demonstrates a common error in Node.js: attempting to start a server on a port that's already in use. The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution.

## Problem
The provided code starts an HTTP server. If port 8080 is already occupied (e.g., by another instance of the server or a different application), the server will fail to start and an error will be thrown. 

## Solution
The solution involves using the `listen` method with an error handler that gracefully handles the `EADDRINUSE` error, which signifies that the address is already in use.  The improved code attempts to restart the server after a short delay if the port is unavailable, providing robustness.