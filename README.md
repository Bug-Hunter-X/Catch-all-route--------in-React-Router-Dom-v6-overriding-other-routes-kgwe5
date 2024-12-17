# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a problem with the catch-all route ('/*') in React Router Dom v6.  The catch-all route unexpectedly intercepts all other routes defined before it, leading to unexpected behavior.

## Problem Description

The issue occurs when defining a catch-all route in `Routes`. While the expected behavior is to catch only routes not explicitly defined, it seems to be overriding all other routes, causing them to never render.

## Solution

The problem can be solved by ensuring that the catch-all route is placed as the last route definition within the `Routes` component.  This allows other routes to be matched before the catch-all route is considered.

## Reproduction

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe that navigating to any route (including '/' and '/about') results in the '404 Not Found' page rendering instead of the expected Home or About components.

## How to fix it

Move the catch-all route to the end of the Route declarations.  See the corrected code in `App.js`.