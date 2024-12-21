# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running operation blocking the event loop. The `server.js` file contains a problematic server implementation. The `serverSolution.js` file provides a solution using asynchronous operations to prevent blocking.

## Problem

The server in `server.js` simulates a long-running operation (5 seconds) within the request handler.  During this time, the event loop is blocked, making the server unresponsive to other requests.  This is a classic example of how synchronous, CPU-bound tasks can cripple a Node.js server.

## Solution

The solution in `serverSolution.js` addresses the issue by using asynchronous operations to prevent blocking of the event loop.  This allows the server to handle multiple requests concurrently, preventing unresponsiveness.