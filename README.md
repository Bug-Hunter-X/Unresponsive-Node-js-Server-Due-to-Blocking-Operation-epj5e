# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler blocks the event loop, making the server unresponsive.  The `server.js` file contains the buggy code, while `serverSolution.js` provides the solution using asynchronous operations.

## Problem

The original server code includes a `while` loop that simulates a long-running task. This task blocks the event loop, meaning no other requests can be processed until the loop completes.  This results in an unresponsive server and poor user experience.

## Solution

The solution involves refactoring the code to use asynchronous operations.  This ensures that the server remains responsive even while long-running tasks are being executed. The `serverSolution.js` shows how to refactor the code using asynchronous pattern and Promises.