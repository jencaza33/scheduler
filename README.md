# Interview Scheduler

Interview Scheduler is a single page React application that allows users to book, edit and cancel interviews.  I have combined a concise API with a WebSocket server to build a realtime experience.

Data is persisted by the API server using a PostgreSQL database and Jest tests were used throughout the development of the project.


## How it Works
When a user loads the Interview Scheduler application, the following page is displayed:

!["Welcome to scheduler"](https://github.com/jencaza33/scheduler/blob/master/docs/1.png?raw=true)

Users can create interviews by clicking on the add + button and inputting their name.  If a name is not indicated, a user will see the following error message:
!["must enter name"](https://github.com/jencaza33/scheduler/blob/master/docs/2.png?raw=true)

The user will then enter their name and select an interviewer, which will be highlighted in white after selection:
!["filling out input form"](https://github.com/jencaza33/scheduler/blob/master/docs/3.png?raw=true)

Once the user clicks the Save button, they will be shown a status indicator while asynchronous operations are in progress:
!["Saving status indicator"](https://github.com/jencaza33/scheduler/blob/master/docs/4.png?raw=true)

Once completed, the user can see their confirmed interview card, displayed in the scheduler:
!["Changes confirmed to appointment"](https://github.com/jencaza33/scheduler/blob/master/docs/5.png?raw=true)

By hovering over their newly created interview, users are able to quickly modify or delete an existing interview by selecting the corresponding icon in the bottom right corner.
!["hover over interview"](https://github.com/jencaza33/scheduler/blob/master/docs/hover-interview.png?raw=true)

When selecting the Delete button, users will first be shown a warning asking if they are sure they want to delete their interview:
!["Confirm delete warning"](https://github.com/jencaza33/scheduler/blob/master/docs/delete-warning.png?raw=true)

Selecting Cancel will bring the user back to regular display. Selecting the Confirm button will proceed with deleting the interview:
!["Delete status indicator"](https://github.com/jencaza33/scheduler/blob/master/docs/deleting-status-indicator.png?raw=true)

In the event that an error occurred while creating or deleting an interview, users will be shown the corresponding errors:
!["Error message when creating apt"](https://github.com/jencaza33/scheduler/blob/master/docs/create-error.png?raw=true)

!["Error message for cancel apt"](https://github.com/jencaza33/scheduler/blob/master/docs/error-delete.png?raw=true)

While interviews are being created or deleted, the number of spots remaining as indicated per day are being updated in realtime.  In this current view, Thursday is fully booked and is clearly displayed as such for a user:
!["spots remaining display"](https://github.com/jencaza33/scheduler/blob/master/docs/final.png?raw=true)

## Dependencies

- [axios](https://axios-http.com/)
- [Babel](https://babeljs.io/)
- [classnames](https://github.com/JedWatson/classnames#readme)
- [Cypress](https://www.cypress.io/)
- [Jest](https://jestjs.io/)
- [prop-types](https://github.com/facebook/prop-types)
- [React](https://reactjs.org/)
- [Storybook](https://storybook.js.org/)
- [Testing Library](https://testing-library.com/)
- [Webpack](https://webpack.js.org/)
- [Webpack Dev Server](https://github.com/webpack/webpack-dev-server)
- [WebSockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API)


## Setup

Install dependencies with `npm install`.

## Running Webpack Development Server

```sh
npm start
```

## Running Jest Test Framework

```sh
npm test
```

## Running Storybook Visual Testbed

```sh
npm run storybook
```