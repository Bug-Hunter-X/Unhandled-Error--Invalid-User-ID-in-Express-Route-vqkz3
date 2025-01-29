# Express.js Unhandled Error: Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input. Specifically, this example shows a route that fetches a user by ID.  If the ID is not a valid number, the code will throw an error. 

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides a corrected version with robust error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install Express.js.
3. Run `node bug.js`.
4. Send a request to `/users/abc` (or any non-numeric ID).

You will observe an error in the console. 

## Solution

The solution in `bugSolution.js` adds input validation to prevent the error. It checks if the `userId` is a valid number before attempting to find the user in the database. If the ID is invalid, it returns an appropriate HTTP error (400 Bad Request).