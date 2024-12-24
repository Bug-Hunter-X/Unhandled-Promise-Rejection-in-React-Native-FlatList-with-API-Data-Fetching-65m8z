# Unhandled Promise Rejection in React Native FlatList

This repository demonstrates a common error in React Native applications involving unhandled promise rejections within FlatList when fetching data from an API.

The issue is that when an error occurs during the data fetching process, the application crashes silently without displaying any error messages. This makes debugging difficult.

The `DataList.js` file contains the buggy code that causes this issue. The `DataListSolution.js` file provides a solution that uses a `try...catch` block within the asynchronous `fetchData` function to handle errors gracefully. It also displays error messages to the user, improving the user experience and aiding in debugging.

## Steps to reproduce

1. Clone this repository.
2. Run the application using `npx react-native run-android` or `npx react-native run-ios`.
3. Observe the app's behavior.  The buggy version will crash silently. The solution will display error messages if the API call fails.

## Solution

The solution is simple: use a `try...catch` block to properly handle potential errors during the API call. This will prevent the application from crashing and provide helpful error messages to the user and developers.