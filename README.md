# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the code attempts to parse a user ID from the request parameters as an integer without verifying if it is a valid integer. This can lead to unexpected behavior or crashes if the ID is not a number.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file provides a corrected version with proper error handling.

## Bug
The primary issue is the lack of input validation before attempting to parse the `userId` as an integer.  If the `userId` is not a valid integer, `parseInt(userId)` will return `NaN`, causing issues later in the code.

## Solution
The solution adds input validation to check if `userId` is a valid integer before attempting to use it.  Additionally, it includes more robust error handling to return appropriate HTTP status codes.