# Introduction

This project is a solution to a technical test for Alinta.

## Requirements

See provide brief [Alinta Coding Test (FE).pdf](./docs/Alinta%20Coding%20Test%20(FE).pdf).

Create a application where;
* User can see list of customers.
* User can search a list of customers by first or last name.
* User can can add a customer.
* User can can edit a customer.
* User can can delete a customer.

## Scope

This scope of this implementation will be limited to;

* Frontend only implementation. No backend or API implementation required. The API will be replicated by a static stub.

## Build Plan

I have put together a build plan which details roughly how I planned to structure the development and each of the feature branches. See [build plan](./docs/BUILD_PLAN.md).

## Notes, Considerations & Potential Improvements

* 

# How to run this project

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Installation

Run `npm install.`

Installation issues
There appears to be some issues with the create-react-script tooling when running `npm install` with newer versions of node see https://github.com/facebook/create-react-app/issues/2613. The install may report some errors and warnings for specific packages not being installed.

To mitigate an issue with the lib `fsevents` not being installed in those cases I have included this library as dev dependency so that `npm run test` will function when running this project on OSX.



## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
