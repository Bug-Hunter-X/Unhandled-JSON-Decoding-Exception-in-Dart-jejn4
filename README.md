# Unhandled JSON Decoding Exception in Dart

This repository demonstrates a common error in Dart applications: neglecting to handle potential exceptions during JSON decoding.  The `jsonDecode` function can throw a `FormatException` if the response body is not valid JSON. This example showcases the error and how to properly handle it using `try-catch` blocks.

## Bug Description

The `bug.dart` file contains code that fetches data from an API, decodes the JSON response, and processes the data. However, it lacks proper error handling for the case where the JSON decoding fails due to an invalid JSON format or other errors.

## Solution

The `bugSolution.dart` file demonstrates the correct way to handle this potential error using a `try-catch` block. It wraps the `jsonDecode` call within a `try` block, and if a `FormatException` (or any other exception) occurs, the `catch` block handles it gracefully, preventing app crashes and providing more informative error messages.