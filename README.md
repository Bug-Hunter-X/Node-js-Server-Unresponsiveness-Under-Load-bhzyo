# Node.js Server Unresponsiveness Under Load

This repository demonstrates a common issue in Node.js servers where they can become unresponsive or hang under heavy load. The problem stems from blocking the event loop with long-running operations.

## Reproducing the Bug

1. Clone this repository.
2. Run `node server.js`.
3. Send a large number of requests to the server (e.g., using tools like `wrk` or `ab`).
4. Observe that the server becomes slow to respond or stops responding entirely.

## Solution

The solution involves using asynchronous operations and techniques like worker threads or message queues to avoid blocking the event loop.

The `server-solution.js` file provides an example using asynchronous operations to mitigate the problem.