# React Router Dom v6 Catch-All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route `/*` in React Router Dom v6. The catch-all route is unexpectedly triggered, even when other routes should match.

## Problem

The provided `App.js` demonstrates a simple React Router setup.  Despite having specific routes for `/` and `/about`, the catch-all route `/` always intercepts navigation, resulting in the `NotFound` component rendering instead of the expected `Home` or `About` components.

## Solution

The issue is resolved in `AppSolution.js`. The solution involves carefully placing the catch-all route at the very end of the `Routes` component. By moving `/*` route after other specific routes, the catch-all route only triggers if no other routes match.