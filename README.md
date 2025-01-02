# React Router v6 Catch-all Route Bug

This repository demonstrates a bug in React Router v6 where catch-all routes (`/*`) are not working as expected. The catch-all route incorrectly matches all paths, preventing other routes from being evaluated. 

## Description

The problem occurs when defining a catch-all route (`/*`) alongside other specific routes.  Instead of acting as a fallback, it seems to match before any other route, causing the intended 'Not Found' component to always render regardless of whether the path is explicitly defined or not.

## Solution

The solution involves reordering the routes in the `Routes` component. By placing the catch-all route at the very end, it ensures it only matches if no other routes are found. This fixes the issue and makes the catch-all route work as intended.