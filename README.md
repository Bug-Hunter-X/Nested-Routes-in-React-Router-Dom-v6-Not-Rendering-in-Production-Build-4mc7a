# React Router Dom v6 Nested Route Issue in Production

This repository demonstrates a problem with nested routes in React Router Dom v6.  The application works correctly in development mode but fails to render nested routes in production builds. The nested routes incorrectly display the 'Not Found' component.

## To Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm run build` to create a production build.
4. Serve the production build (e.g., using `serve -s build`).
5. Navigate to a nested route. You will see the 'Not Found' component instead of the expected nested route component.

## Solution

The provided solution addresses the issue by ensuring that the nested routes are correctly defined within the parent route's `element` prop. The key fix involved restructuring how the nested routes were handled in the main App component.