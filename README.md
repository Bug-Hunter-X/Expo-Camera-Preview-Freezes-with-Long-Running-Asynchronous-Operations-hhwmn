# Expo Camera Preview Freeze Bug

This repository demonstrates a bug where the Expo Camera component's preview freezes or displays a blank screen when performing long-running asynchronous operations. The issue arises from the camera component's state being updated while the asynchronous task is still in progress, potentially leading to unmounting or rendering issues.

## Reproducing the Bug

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `expo start` to start the Expo development server.
4. Observe the camera preview.  You might see it freeze or show a blank screen if the API request takes a noticeable amount of time to complete.

## Solution

The solution involves ensuring that the camera component is not unmounted or updated in such a way that it results in it being unable to refresh its preview.  A proper approach would involve managing the asynchronous operations effectively and preventing state changes that could adversely affect the camera component. Please view `bugSolution.js` for implementation details.

## Technologies Used

* Expo
* React Native
* JavaScript