# Express.js JSON Request Body Parsing Error

This repository demonstrates a common error in Express.js applications where the request body is not parsed correctly when receiving JSON data. The `req.body` object remains empty, causing unexpected behavior or application crashes.

## Bug

The `bug.js` file shows an Express.js server that attempts to process JSON data from a POST request.  However, due to the improper or missing use of middleware, the JSON data is not parsed correctly, leading to an empty `req.body` object.  The server receives the request and logs `req.body`, but the log will be empty.

## Solution

The `bugSolution.js` file presents the corrected version. The solution involves using the `express.json()` middleware to parse incoming JSON requests before the request handling route.  This correctly populates the `req.body` object with the JSON data sent in the POST request.

## Setup

1. Clone this repository.
2. Navigate to the repository in your terminal.
3. Run `npm install` to install necessary dependencies.
4. Run `node bug.js` to observe the bug.
5. Run `node bugSolution.js` to see the solution in action.