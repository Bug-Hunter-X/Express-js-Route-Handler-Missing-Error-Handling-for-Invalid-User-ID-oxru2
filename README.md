# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the code attempts to parse a user ID from the request parameters without checking if the ID is a valid integer. This can lead to unexpected behavior or crashes if the user ID is not a number.

## Bug

The `bug.js` file contains the erroneous code.  The route handler for `/users/:id` attempts to find a user based on the provided ID. However, it does not handle the case where the ID is not a number or is not found in the `users` array.

## Solution

The `bugSolution.js` file provides a corrected version of the code.  It includes error handling to check if the `userId` is a number and if the user exists.  If the user ID is invalid, a 404 (Not Found) error is returned.