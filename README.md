# Silent Crash in Express.js App

This repository demonstrates a silent crash bug in an Express.js application. The application appears to start successfully, but attempting to access the root route results in a crash without any error messages in the console.

## Bug Description

The issue lies in the `res.send()` method within the `app.get` handler.  The problem is subtle and can be easily overlooked, especially for beginners or when dealing with more complex applications.  The application simply crashes without any informative output, making debugging difficult.

## Solution

The solution involves proper error handling and logging to identify the source of the crash. In this case, we use a `try...catch` block to handle potential exceptions and ensure that any errors encountered during the request processing are logged to the console.