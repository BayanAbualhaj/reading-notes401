# Redux - Additional Topics

![](https://res.cloudinary.com/practicaldev/image/fetch/s--o5hN-7gH--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/gz8ddo8zehhn1djkm42h.png)

## What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?

The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app.

________________________

## When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

the async function.

_____________________

## terms:

* **middleware**: Redux middleware provides a third-party extension point between dispatching an action, and the moment it reaches the reducer. People use Redux middleware for logging, crash reporting, talking to an asynchronous API, routing, and more.

* **thunk**: Redux Thunk is middleware that allows you to return functions, rather than just actions, within Redux. This allows for delayed actions, including working with promises. One of the main use cases for this middleware is for handling actions that might not be synchronous, for example, using axios to send a GET request. 

__________________________________

## Redux Toolkit was originally created to help address three common concerns about Redux:

* "Configuring a Redux store is too complicated"
* "I have to add a lot of packages to get Redux to do anything useful"
* "Redux requires too much boilerplate code"

___________________________

## What's Toolkit includes

* A configureStore() function with simplified configuration options. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.
* A createReducer() utility that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the immer library to let you write simpler immutable updates with normal mutative code, like state.todos[3].completed = true.
* A createAction() utility that returns an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.
* A createSlice() function that accepts a set of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.
* The createSelector utility from the Reselect library, re-exported for ease of use.
