# Express.js Route Handler Missing Return Statement Bug

This repository demonstrates a common error in Express.js route handlers: omitting the `return` statement in a conditional branch.  This can lead to unexpected behavior and errors.

## Bug Description

The `bug.js` file contains an Express.js route handler that fetches a user based on their ID. If the user is not found, the handler sends a 404 status. However, it omits the `return` statement. This leads to the handler continuing execution, potentially sending an unintended response, hanging the client, or leading to unpredictable results.

## Solution

The `bugSolution.js` file provides the corrected code. The addition of `return` ensures that the handler exits cleanly when the user is not found, properly sending the 404 response.