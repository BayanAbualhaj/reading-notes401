# Redux - Combined Reducers


![](https://res.cloudinary.com/practicaldev/image/fetch/s--lagavvso--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/gv3ypw62p54qeawyu6ac.png)


## Why choose Redux instead of the Context API for global state?

Redux is the industry standard for managing state of large applications, so it is important to know well. It is more optimized for larger projects, because the context API re-renders more often.

_____________________

## What is the purpose of a reducer?

A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. We have tools, like Redux, that help manage an application's state changes in a single store so that they behave consistently.

______________________

## What does an action contain?

Object literals that tell the reducer what is being done to the app, and any data required for the update.

___________________

## Why do we need to copy the state in a reducer?

Then the function uses a switch statement to determine which type of action it’s dealing with. If there is an unknown action, then it should return the state , so that the application doesn’t lose its current state.

________________________

## Terms:

* **immutable state:** Immutable state is state that cannot be changed. Immutable objects (for which none of the state can be changed) become important when you are dealing with concurrency, the ability for more than one processor in your computer to operate on that object at the same time.

* **time travel in redux:** The Redux DevTools records dispatched actions and the state of the Redux store at every point in time. This makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app.

* **action creator:** is merely a function that returns an action object. Redux includes a utility function called bindActionCreators for binding one or more action creators to the store’s dispatch() function.

* **reducer:** is a pure function that takes the current state and an action, and returns the next state. Note that the state is accumulated as each action on the collection is applied to change this state. So given a collection of actions , the reducer is applied on each value of the collection (from left-to-right).

* **dispatch:** Dispatch is the act of sending something somewhere. In computer science, this term is used to indicate the same concept in different contexts, like to dispatch a call to a function, dispatch an event to a listener, dispatch an interrupt to a handler or dispatch a process to the CPU.

___________________

* **combineReducers** The most common state shape for a Redux app is a plain Javascript object containing “slices” of domain-specific data at each top-level key. Similarly, the most common approach to writing reducer logic for that state shape is to have “slice reducer” functions, each with the same (state, action) signature, and each responsible for managing all updates to that specific slice of state. Multiple slice reducers can respond to the same action, independently update their own slice as needed, and the updated slices are combined into the new state object.

* **State Shape** There are two ways to define the initial shape and contents of your store’s state. First, the createStore function can take preloadedState as its second argument. This is primarily intended for initializing the store with state that was previously persisted elsewhere, such as the browser’s localStorage. The other way is for the root reducer to return the initial state value when the state argument is undefined. These two approaches are described in more detail in Initializing State, but there are some additional concerns to be aware of when using combineReducers.

