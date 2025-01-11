# React Router v6 Catch-all Route Issue

This repository demonstrates a subtle bug in React Router v6 related to the placement of catch-all routes (`/*`) within nested `Routes` components.  When a catch-all route is nested, it doesn't function as expected, potentially leading to unexpected routing or rendering issues. 

## Problem Description

The `App.js` file contains a simple React Router setup with a home route, an about route, and a catch-all route for 404 errors.  When the catch-all route (`/*`) is nested within the `Routes` component, the application fails to properly handle routes that don't match the other defined paths.  The expected behavior is that the catch-all route should handle any unmatched paths. However, the issue is that the catch-all route does not function when inside the Routes component.  

## Solution

The solution, demonstrated in `AppSolution.js`, involves moving the catch-all route outside the nested `Routes` component. This ensures that it correctly intercepts any unmatched paths and renders the 404 page appropriately. 

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to a path that doesn't match `/` or `/about` (e.g., `/nonexistent`). You'll observe the unexpected routing behavior in `App.js` and the correct handling of unmatched paths in `AppSolution.js`.
