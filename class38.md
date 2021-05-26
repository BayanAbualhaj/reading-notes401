# Redux - Asynchronous Actions

![](https://i.ytimg.com/vi/KTOoHu7kJTY/maxresdefault.jpg)

## How granular should your reducers be?

Some developers prefer to have “fat” action creators, with “thin” reducers that simply take the data in an action and blindly merge it into the corresponding state. Others try to emphasize keeping actions as small as possible, and minimize the usage of getState() in an action creator.

__________________

## Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched

When your reducer has finished and returned the new application state, asyncDispatch will trigger store. dispatch with whatever action you give to it. You might try using a library like redux-saga.

_______________________

## Name a strategy for preventing the above

Using switch

___________________

## Terms:

* **store**:A store is an immutable object tree in Redux. A store is a state container which holds the application's state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer.

* **combined reducers**:The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore . The resulting reducer calls every child reducer, and gathers their results into a single state object.

___________________

## Some common kinds of side effects are things like
1. Logging a value to the console
2. Saving a file
3. Setting an async timer
4. Making an AJAX HTTP request
5. Modifying some state that exists outside of a function, or mutating arguments to a function
6. Generating random numbers or unique random IDs (such as Math. random() or Date.now())


______________________

## Redux Thunk
Redux Thunk is middleware that allows you to return functions, rather than just actions, within Redux. This allows for delayed actions, including working with promises. One of the main use cases for this middleware is for handling actions that might not be synchronous, for example, using axios to send a GET request.

_____________________

