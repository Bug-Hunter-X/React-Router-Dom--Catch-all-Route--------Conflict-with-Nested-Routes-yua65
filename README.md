# React Router Dom Catch-all Route Bug

This repository demonstrates a subtle bug in React Router Dom v6 related to the interaction between catch-all routes (`/*`) and nested routes.  In certain configurations, the catch-all route incorrectly intercepts requests that should be handled by nested routes.

## Problem Description

The problem occurs when a catch-all route is present alongside nested routes. Under specific conditions, the catch-all route is activated even if a valid nested route matches the URL, leading to unexpected 404 errors or incorrect component rendering.

## Solution

The solution involves careful route ordering and potentially restructuring route definitions. The provided `AppSolution.js` shows one possible fix.  The key might be to avoid having a catch all route if nested routes are expected to handle all paths. 

## Reproduction

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install`.
4. Run `npm start`.
5. Observe the unexpected behavior.  Navigate to the nested routes and notice the `404 Not Found` page may appear when it shouldn't.
