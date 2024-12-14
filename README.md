# Node.js Server Hang: Synchronous Long Operation

This repository demonstrates a common Node.js issue: a server hanging due to a long-running synchronous operation within the request handler.  The provided `server.js` file shows a simple HTTP server that performs a 5-second CPU-bound task. This blocks the event loop, preventing the server from responding to further requests.

The `serverSolution.js` file provides a solution that uses asynchronous operations and demonstrates proper handling of long-running tasks to prevent the server from becoming unresponsive.

**How to Reproduce:**
1. Clone this repository.
2. Run `node server.js`.
3. Open your browser to `http://localhost:3000`.  You'll see the response, but any subsequent requests will hang until the first request completes.

**Solution:**  The solution uses asynchronous techniques to handle long-running operations and prevents blocking of the event loop.