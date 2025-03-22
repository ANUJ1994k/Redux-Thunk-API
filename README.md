# redux-user-management
Create a Redux store to manage the state of a list of users fetched from an API. Use redux-thunk middleware to handle asynchronous actions.

# redux-user-management App

A React application that demonstrates Redux state management with Thunk middleware to handle asynchronous API calls. This project displays user data fetched from a public API and shows both a list view and detailed user information.

## Features

- Fetches user data from JSONPlaceholder API
- Manages application state with Redux
- Handles asynchronous operations with Redux Thunk
- Implements client-side routing with React Router
- Displays loading spinners during API requests
- Shows detailed user information on a separate page

## Project Structure

```
src/
├── components/
│   ├── HomePage.js
│   ├── UserDetailsPage.js
│   └── LoadingSpinner.jsx
      └── LoadingSpinner.css
├── redux/
│   ├── store.js
│   ├── userReducer.js
│   └── userActions.js
├── App.js
└── index.js
```

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/redux-user-management.git
   cd redux-user-management
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Start the development server:
   ```
   npm start
   ```

## Dependencies

- React
- Redux
- Redux Thunk
- React Router DOM
- Axios

## Usage

### Home Page

The home page displays a list of user names fetched from the API. Each name is a clickable link that navigates to the user details page.

### User Details Page

The user details page displays comprehensive information about a specific user, including:
- Name
- Email
- Phone
- Address
- Company information

A "Back to Home" button allows navigation back to the user list.

## Redux Implementation

### Store

The Redux store is set up in `store.js` with Thunk middleware to handle asynchronous actions.

### Reducer

The user reducer in `userReducer.js` manages the application state, including:
- User data
- Loading status
- Error information

### Actions

Actions in `userActions.js` include:
- `FETCH_USERS_REQUEST`: Indicates a request is in progress
- `FETCH_USERS_SUCCESS`: Indicates a successful data fetch
- `FETCH_USERS_FAILURE`: Indicates an error occurred

The `fetchUsers` thunk action creator handles the asynchronous API call to retrieve user data.

## Routing

React Router is used to handle navigation between pages:
- `/`: Home page showing the list of users
- `/user/:id`: User details page showing detailed information for a specific user

## Loading States

A spinner component is displayed during API calls to provide visual feedback to users.

## Future Enhancements

Potential improvements for this project:
- Add the ability to create, update, and delete users
- Implement form validation
- Add search and filtering capabilities
- Implement pagination for larger data sets
- Add unit tests
- Enhance UI with a component library like Material-UI or Bootstrap

